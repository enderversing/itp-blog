# Week 2

## Traceroute Exercise

**are.na**
![are.na map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/arena_map.png)
![are.na terminal](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/terminal/arena.png)

**arena.computer**
![arena.computer map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/arenacomputer_map.png)
![arena.computer terminal](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/terminal/arena_computer.png)
**dodoskin.com**
![dodoskin map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/dodoskin_map.png)
![dodoskin terminal](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/terminal/dodoskin.png)
**douyin.com**
![douyin map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/douyin_map.png)
**google.com**
![google map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/google_map.png)
![google terminal](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/terminal/google.png)
**proton.me**
![proton map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/proton_map.png)
![proton terminal](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/terminal/protonmail.png)
**stylevana.com**
![stylevana map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/stylevana_map.png)
![stylevana terminal](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/terminal/stylevana.png)
**the-qi.com**
![qi map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/the_qi_map.png)
![qi terminal](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/terminal/the_qi.png)
**tiktok.com**
![tiktok map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/tiktok_map.png)
![tiktok terminal](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/terminal/tiktok.png)
**yesstyle.com**
![yesstyle map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/yesstyle_map.png)
![yesstyle terminal](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/terminal/yesstyle.png)
**youtube.com**
![youtube map](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/maps/youtube_map.png)
![youtube terminal](https://enderversing.github.io/itp-blog/assets/img/undnet/week2/terminal/youtube.png)

These are the autonomous systems I ran into during this exercise most frequently. 
* AS0
    * I think this is NYU.
*  AS19905
    * DigiCert.
* AS3356
    * Lumen
* AS12
    * This is New York University.
* AS13335
    * Cloudflare.
## Readings

### On Distributed Communications



This is the paper talking about the design of the Internet as a network that could survive military attacks! So fascinating.


What is adaptive store-and-forward? Is it possible for store-and-forward routed devices to have permanent memory without a centralized server or "cloud"? The idea of recent history of network traffic being used to modify path selection reminds me of the design of the Solar Protocol. 

When I learned of the Solar Protocol's design, I found it naive, but some of what I found naive is similar to how the Internet works. I always assume that everything in the human world, hardware or software, has been meticulously designed using esoteric algorithms and data structures. I am shocked when I turn out to be wrong.*


I wonder why "a standard format message block" would enable real-time voice over Internet? Meshtastic is a radio network that uses store-and-forward routing but struggles to enable voice transmission of any kind, let alone real time.

I will always find the distributed network more beautiful than the decentralized network. Maybe I'm simple. There's a kind of purity of thought and simplicity there which I find very appealing.

I am not sure how the minimum span of a network is related to the decentralized network's "redundancy level". (Frankly, I'm still not sure what the minimum span is.)

I love talking about noise. Information theory, here we go!** 

I'm really excited to have this reference because, even more than the content in the piece, I'm happy to concretely be able to point to an example of how military operations shaped the development of the Internet. I have read about or around this subject, but never have I accessed a primary source of this nature.

Why do switching systems need to try a subset of potential paths that can be drawn on a gridded network? I may be misunderstanding the problem here, but couldn't these paths be predicted? If there is a need to try paths instead of using an algorithm to predict them, I would suspect that switching is actually a computationally difficult problem?


> We will soon be living in an era in which we cannot guarantee survivability of any single point. However, we can still design systems in which system destruction requires the enemy to pay the price of destroying n of n stations. If n is made sufficiently large, it can be shown that highly survivable system structures can be built—even in the thermonuclear era.
    


I think this piece is shortsighted, but probably written with the best foresight the author could imagine in their time. Right now, we see "system destruction" from time to time in the form of outages. I can only imagine these outages become more and more bombastic if or when quantum computers become less noisy***.

I have been reading a book with a great title - *Why Hackers Win* - which discusses how the Internet is actually becoming more centralized, and therefore, less stable, as time progresses.


#### Footnotes

*I like when I find complexity in the design of everyday "things". I was reading books about music last week and a few of them mentioned the design of the MP3 as a compression format designed to be transported over networks. I always assume that all digital creations are complex or wordlessly deep.

**I still don't really understand information theory, I've just read the first chapter of one highly esteemed book on the subject over and over.

***Quantum computers could be the end of the Internet, or merely the next coming of dishonest tech startups - I'm not sure yet.


### Stupid Networks

Honestly, I don't understand this piece. What is the stupid protocol? Is it...the Internet? How is the Internet stupid?
