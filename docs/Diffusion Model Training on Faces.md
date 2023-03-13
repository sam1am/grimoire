Following this tutorial: 

https://www.youtube.com/watch?v=dfMLrytpfAU

Training images needed: ~10 (up to 20 or 30 but it takes longer) 
- High quality
- Various lighting
- Various pose
- Various angles

Resize all to 512x512

Some more info here: [Stable Diffusion Training for Personal Embedding (bennycheung.github.io)](https://bennycheung.github.io/stable-diffusion-training-for-embeddings) 

According to Jame Cunliffe’s [video](https://www.youtube.com/watch?v=P1dfwViVOIU&ab_channel=JAMESCUNLIFFE), we learned that only 20 images are sufficient.

-   3 full body with different angle
-   5 half body with different angle
-   12 close-up with different angle and facial expressions
-   I am a little paranoid - just give it a little more

The training process expects the images you provide are of dimension 512x512. If your images are of a different size, you can use [Birme](https://www.birme.net/?target_width=512&target_height=512) to adjust and resize the images so they match the proper requirements for the neural network to read.

### Training Prompt

A portrait of a man, trending on artstation, greg rutkowski, 4k