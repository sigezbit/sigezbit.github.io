---
layout: post
title: "2. Sprites and costumes"
topic_slug: "scratch"
order: 2
---

Let's create a new project. To do this, select "New" from the "File" menu. Now look at the lower right corner—at the sprites area.

![Sprites]({{ "/assets/images/scratch/sprites.png" | relative_url }})

In Scratch, all characters and objects that appear on the stage are called **sprites**. Even our kitten in the sprites area is labeled as "Sprite 1".

A single program can have many characters. To add a new friend for Scratch, hover your mouse over the purple cat face icon in the lower right corner. A menu will open where you can choose a character from the library, draw your own, or upload an image from your computer.

![Sprites menu]({{ "/assets/images/scratch/sprites-menu.png" | relative_url }})

Let's pick a character from the library. Click the cat face or the magnifying glass—a list of Scratch's friends and various objects will open. To find what you need faster, use the search field: type "dance", and only the dancers will stay on screen. If you hover your mouse over a character, they will show off their dance moves. Select "Cassy Dance".

Now Cassy is on the stage! You can drag her anywhere with your mouse. Let's give her a boombox—in the library, it's called "Radio". And we can remove the kitten, since he doesn't really care for loud music. To do this, click the kitten icon below the stage and click the trash can icon.

![Remove sprite]({{ "/assets/images/scratch/sprites-remove.png" | relative_url }})

Now all that's left is to add a dance-worthy backdrop! Click the button with the picture in the lower right corner (next to the sprite button) to choose one. For our disco party, the "Concert" backdrop is a perfect fit.

![Backdrops menu]({{ "/assets/images/scratch/sprites-backdrop.png" | relative_url }})

Now let's turn on some music. Select the radio sprite, and in the upper left corner, switch to the "Sounds" tab. There are already a few standard sounds here, but they aren't quite right for a disco. Let's find something from the sound library. Click the purple speaker icon in the bottom corner of the window and find the sound "Dance Around".

![Choose sound]({{ "/assets/images/scratch/sprites-sounds.png" | relative_url }})

To make the music start as soon as the program runs, go back to the "Code" tab and build this script: attach a yellow "When flag clicked" header block, connect an orange "forever" block to it, and insert a magenta "play sound Dance Around until done" block inside. Now, when you click the green flag, music will start playing!

![Radio code]({{ "/assets/images/scratch/sprites-radio-code.png" | relative_url }})

But Cassy isn't dancing yet! To fix that, first stop the music by clicking the red circle next to the flag. Select the Cassy sprite and add a similar program for her: add a yellow "When flag clicked" header block, followed by an orange "forever" block. Inside the loop, insert a purple "next costume" block and an orange "wait 1 seconds" block. Let's change the 1 to 0.2 (use a period, not a comma) so Cassy dances to the right beat.

On the "Costumes" tab, you can see that Cassy has four different poses. In Scratch, these are called **costumes**. Our program will switch between them one by one, like frames in an animated cartoon, bringing Cassy to life. Run the program and watch her dance!

![Cassy code]({{ "/assets/images/scratch/sprites-cassy-code.png" | relative_url }})

> If Cassy is dancing too fast or too slow, simply change the number in the "wait" block.

Awesome! Let's give her some company—the "Ten80 Dance" sprite from the sprite library. If he looks a bit too big, change his size in the field below the stage (for example, to 70), and drag him to an open spot.

To make Ten start dancing too, Cassy can "teach" him. Select the Cassy sprite below the stage, open the "Code" tab, grab her script by the top header block, and drag it right onto the Ten80 icon in the sprites panel below the stage. When Ten80's icon wiggles—let go! The script is copied. Now, if you restart the program, both of our characters will be dancing.

> To restart the program, click the red circle and then click the flag above the stage.

You can also create a separate program for the backdrop. Select the backdrop in the lower right corner and switch to the "Code" tab in the upper left corner. Some blocks aren't meant for backdrops, so they won't appear when a backdrop is selected instead of a sprite. Add a yellow "when flag clicked" block and attach an orange "forever" block. Inside, insert a purple "change color effect by 25" block and an orange "wait 1 seconds" block. Change 1 second to "0.1".

![Result]({{ "/assets/images/scratch/sprites-result.png" | relative_url }})

What we've learned:

- Manage sprites: add characters, resize them, and remove unwanted ones.
- Set the scene: choose backdrops and work with the sound library.
- Animate: switch character costumes, turning still pictures into motion.
- Copy code: quickly share scripts from one character to another.

**Starred task**: Try changing the effects and the number in the "change color effect by 25" block in the backdrop code. To see the change take effect, restart the program.
