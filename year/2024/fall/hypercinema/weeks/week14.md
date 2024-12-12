## Week 14

For my Hypercinema and ICM: Media finals, I worked on a Cornell Box.


![hero gif](https://enderversing.github.io/itp-blog/assets/img/hypercinema/hero.gif)

I had a consistent issue with HDR skyboxes crashing Godot on my personal computer.
![hdr glitch](https://enderversing.github.io/itp-blog/assets/img/hypercinema/doc/1.png)

I used an AI tool to generate a 3D model of Nelson Mandela's house, which was nice. When I first imported it, the orientation seemed random.
![red house 3D model rotated in air](https://enderversing.github.io/itp-blog/assets/img/hypercinema/doc/2.png)


I needed to rotate the mesh to have it lying flat on the ground/y-axis (y=0). 
![red house 3D model flat on ground](https://enderversing.github.io/itp-blog/assets/img/hypercinema/doc/3.png)

The generated 3D model was malformed, which I "fixed" by hiding the model's asymmetry under the y-axis.
![asymmetrical red house 3D model](https://enderversing.github.io/itp-blog/assets/img/hypercinema/doc/4.png)

I thought this HDR looked really nice but it kept crashing my computer.
![HDR crash reimport screen](https://enderversing.github.io/itp-blog/assets/img/hypercinema/doc/5.png)

I started to realize that I would not be able to use HDRs for skyboxes in Godot like I had intended.
![HDR crash reimport screen again](https://enderversing.github.io/itp-blog/assets/img/hypercinema/doc/6.png)

I tried to work with a completely black skybox instead. However, when I imported the resulting glTF into Google Model Viewer, the black skybox had disappeared. 
![black skybox](https://enderversing.github.io/itp-blog/assets/img/hypercinema/doc/7.png)

Thankfully, Google Model Viewer has its own skybox editing tool. 
![Google Model Viewer](https://enderversing.github.io/itp-blog/assets/img/hypercinema/doc/8.png)
