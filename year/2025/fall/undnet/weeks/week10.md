# Week 10


Base URL: `https://starling.directory/api`

This REST API exposes a simple JSON file–backed catalog of “problems.” You can list, filter, read, create, update, and delete problems.

> Content type: JSON (`application/json`)

---


### Example object

```json
{
  "Problem_Title": "Divergence implies arithmetic progressions.",
  "Problem_Summary": "If the sum of the reciprocals of a set of positive integers is infinite, must the set contain arbitrarily long finite arithmetic progressions?",
Cash_Award:	"$3000 USD (Fixed, Paul Erdős)",
  "Research_Area": "Number Theory",
}
```

---

## Endpoints

### 1) List all problems

`GET /api`

Returns the full array from `problems.json`.

**Response 200**

```json
[
  { "Problem_Title": "...", "Problem_Summary": "...",  "Cash_Award": "...", "Research_Area": "..." },
]
```

---

### 2) Filter problems

`GET /api/filter`

Query parameters (all optional):

| Param          | Type          | Behavior                                                                                                              |
| -------------- | ------------- | --------------------------------------------------------------------------------------------------------------------- |
| `researchArea` | string        | Case-insensitive `includes` match against `Research_Area`.                                                            |
| `cashAward`    | string/number | Parsed to a number (currency symbols/commas ignored). Returns problems with `Cash_Award` **greater than** this value. |

Notes:

* `researchArea` → `"number theory"` matches `"Number Theory, Diophantine Equations"` (case-insensitive substring).
* `cashAward` → both `"5000"` and `"$5,000"` are accepted. In data, `Cash_Award` is parsed similarly (e.g., `"$7,500"` → `7500`).

**Example requests**

```
GET /api/filter?researchArea=quantum
GET /api/filter?cashAward=200
GET /api/filter?researchArea=quantum&cashAward=200
```

**Response 200**

```json
[{
"Problem_Title":"Yang-Mills & the Mass Gap",
"Problem_Summary":"Experiment and computer simulations suggest the existence of a “mass gap” in the solution to the quantum versions of the Yang-Mills equations. But no proof of this property is known.",
"Cash_Award":"$1,000,000 USD (Fixed, Clay Mathematics Institute)",
"Research_Area":"Quantum Physics, Mathematical Physics"
}]
```

---

### 3) Get a problem by title

`GET /api/:title`

Looks up a single problem by **exact title match** (case-insensitive). The entire `:title` path segment is compared to the stored `Problem_Title`.

> Tip: URL-encode titles that contain spaces or special characters.
> Example: `GET /api/p%20vs%20np`

**Response 200**

```json
[{
"Problem_Title":"P vs NP",
"Problem_Summary":"If it is easy to check that a solution to a problem is correct, is it also easy to solve the problem? This is the essence of the P vs NP question.",
"Cash_Award":"$1,000,000 USD (Fixed, Clay Mathematics Institute)",
"Research_Area":"Computer Science, Computational Complexity Theory"
}]
```

---

### 4) Create a problem

`POST /`

Body: JSON object.

**Request**

```http
POST / HTTP/1.1
Content-Type: application/json

{
  "Problem_Title": "Federated Audio Denoising",
  "Problem_Summary": "Train a denoiser on-device without sharing raw audio.",
  "Research_Area": "ML, Privacy",
  "Cash_Award": "$5,000"
}
```

**Responses**

* **201**

  ```json
  {
    "Problem_Title": "Federated Audio Denoising",
    "Problem_Summary": "Train a denoiser on-device without sharing raw audio.",
    "Research_Area": "ML, Privacy",
    "Cash_Award": "$5,000"
  }
  ```


---

### 5) Update a problem (merge)

`PUT /:title`

Merges the provided fields into the existing problem identified by the exact (case-insensitive) title. Fields not included remain unchanged.

**Request**

```http
PUT /Federated%20Audio%20Denoising HTTP/1.1
Content-Type: application/json

{ "Cash_Award": "$7,500" }
```

**Response 200**

```json
{
  "Problem_Title": "Federated Audio Denoising",
  "Problem_Summary": "Train a denoiser on-device without sharing raw audio.",
  "Research_Area": "ML, Privacy",
  "Cash_Award": "$7,500"
}
```


---

### 6) Delete a problem

`DELETE /:title`

Deletes the problem with a matching (case-insensitive) title.

**Response 200**

```json
[
  {
    "Problem_Title": "Federated Audio Denoising",
    "Problem_Summary": "Train a denoiser on-device without sharing raw audio.",
    "Research_Area": "ML, Privacy",
    "Cash_Award": "$7,500"
  }
]
```

> Note: The API returns an array containing the deleted object (the result of `Array.splice`).

**Response 404**

```json
{ "message": "Problem not found" }
```

---

## cURL examples

```bash
# List all problems
curl -s https://starling.directory/api/

# Filter by research area
curl -s "https://starling.directory/api/filter?researchArea=nlp"

# Filter by minimum cash award (> 5000)
curl -s "https://starling.directory/api/filter?cashAward=5000"

# Get one by title (URL-encode spaces/special chars)
curl -s "https://starling.directory/api/Robust%20Few-Shot%20OCR"

# Create
curl -s -X POST https://starling.directory/api/ \
  -H "Content-Type: application/json" \
  -d '{
    "Problem_Title": "Self-Supervised Birdsong ID",
    "Problem_Summary": "Identify species from short clips with minimal labels.",
    "Research_Area": "Bioacoustics, ML",
    "Cash_Award": "$3,000"
  }'

# Update (partial merge)
curl -s -X PUT "https://starling.directory/api/Self-Supervised%20Birdsong%20ID" \
  -H "Content-Type: application/json" \
  -d '{ "Cash_Award": "$4,000" }'

# Delete
curl -s -X DELETE "https://starling.directory/api/Self-Supervised%20Birdsong%20ID"
```
---

Disclosure: In return for/as a benefit of attending [this conference](https://www.let-all.com/), I was given a free ChatGPT Enterprise subscription, which I used to generate these docs.
