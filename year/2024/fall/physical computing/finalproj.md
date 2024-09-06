# Final Project 


I am bored! I am thinking about the future. I may as well plan my final project.

**What is this document?**

I know that I want to do something in tangible computing, but I don't have links to any resources explaining what I mean by "tangible computing".

I've read a lot of studies about tangible computing enabling accessible interfaces, but I never thought to save any of those links...

## Brainstorming
`9.5.24`
I know that the tangible computing labs at [MIT](https://tangible.media.mit.edu) and [Stanford](https://shape.stanford.edu/) have produced papers I read before.


I think I remember reading [shapeCAD: An Accessible 3D Modelling Workflow for the
Blind and Visually-Impaired Via 2.5D Shape Displays](https://shape.stanford.edu/research/shapeCAD/shapeCAD-Paper_ASSETS19.pdf) and being very impressed! This is the kind of interface I have in mind for the interactive fiction game console.

Apparently what I'm interested in is called [*tactile graphics*](https://ieeexplore.ieee.org/abstract/document/5227855) - interfaces that allow you to *feel* an image.

I was thinking the interactive fiction console should allow you to read by touching tactile Braille "images," but it seems that [Braille is not always...accessible](https://dl.acm.org/doi/fullHtml/10.1145/3544548.3580844)? I'm not sure what the text format should be. I could have interpreted [that study](https://dl.acm.org/doi/fullHtml/10.1145/3544548.3580844) incorrectly.

I see that I could be inspired by existing [refreshable braille displays](https://en.wikipedia.org/wiki/Refreshable_braille_display) instead of starting from scratch. [That wiki](https://en.wikipedia.org/wiki/Refreshable_braille_display) says that speech synthesis is often used in combination with the braille display. 

I wonder if [self-voicing](https://www.renpy.org/doc/html/self_voicing.html) could be added to Twine games? [RenPy](https://www.renpy.org) relies on the operating system for speech synthesis, but Twine operates in the browser and may not have access to that part of the OS. Self-voicing is not available in Chrome OS.

The Microsoft Speech API is a possibility, but I assume it costs money. There's also the possibility of using some [TensorFlow](https://js.tensorflow.org/index.html)/[ONNX](https://github.com/microsoft/onnxruntime) model, but it makes me feel sketchy. I think it would *probably* be decently easy in TensorFlow but I don't feel good about it.

I found an [ONNX model](https://k2-fsa.github.io/sherpa/onnx/tts/wasm/index.html) for [text to speech](https://en.wikipedia.org/wiki/Speech_synthesis). Strangely, no one has compiled [eSpeak](https://en.wikipedia.org/wiki/ESpeak) to WebAssembly yet ([successfully](https://github.com/WebAssembly/binaryen/discussions/5749)).

This actually seems like it would be...quite easy...once I decide on the elements included in the game console's design.

I'm not trying to do anything that has not been done before - this is just a new combination things that already exist.


