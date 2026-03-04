---
layout: post
title: "Hello, Scratch!"
topic_slug: "scratch"
order: 2
---

So, shall we get started? You can open the Scratch programming environment directly in your browser. To do this, go to [https://scratch.mit.edu/](https://scratch.mit.edu/) and click "Create" in the upper left corner. When you first launch, you can change the interface language or adjust the contrast in the top menu.

![Scratch Menu]({{ "/assets/images/scratch/main-window-menu.png" | relative_url }})

Now you're ready to get creative! However, to save and share your projects directly on the Scratch website, you'll need to create an account. To do this, your young programmer will need help from their parents.

> Important: To confirm your account and share projects, you must click the link in the email sent to your parents.

If your computer has an older operating system or an unstable internet connection, you can download and install the offline editor from the website: [https://scratch.mit.edu/download](https://scratch.mit.edu/download).

Now let's take a closer look at the Scratch interface – it's very simple and intuitive.

![Scratch Interface]({{ "/assets/images/scratch/main-window.png" | relative_url }})

It consists of four main parts:

1. **Workspace** (center): This is our "table." This is where we'll drag blocks and assemble them into instructions.
2. **Scene** (upper right): Our "window" into the game world. Here you can see the results of your work and how the characters behave.
3. **Block Palette** (left): Our "toolbox." All blocks are divided into groups of different colors to make them easier to find by meaning: Movement, Appearance, Sound, Events, and others.
4. **Sprite Area** (bottom right): This is where all the characters and objects live. Currently, there's only one character there.

Look at the stage – our first character has already appeared. Meet Scratch the kitten! For now, he's just a still image, but we'll bring him to life with code. Let's create our first program so Scratch can say hello.

## Creating Your First Program

On the left side of the screen, click the yellow "Events" circle and drag the "When Sprite is Clicked" block to the workspace. It has a mound at the top and a ridge at the bottom. These blocks are called "header blocks," and they're the starting point for any program.

Now click the purple "Appearance" circle and find the "Say *Hello!* for *2* seconds" block. It has a notch at the top and a ridge at the bottom, just like a "header block." These blocks are called "stack blocks." They can be connected to each other from both the top and bottom, creating long chains of commands.

Connect these two blocks together like puzzle pieces. If they don't click the first time, move them closer together to "magnetize" them.

Now click on the word "Hello!" inside the block and add: "My name is Scratch!"

![Hello Scratch]({{ "/assets/images/scratch/main-window-hello.png" | relative_url }})

Congratulations, our first program is ready! Now just click on the kitten right on the stage, and he'll say hello.

Besides header blocks and stack blocks, Scratch has other block shapes:

- **Logic blocks** are hexagonal in shape. They contain a condition, such as "Is the mouse pointer touching?" or "Is the spacebar pressed?" These blocks answer questions that can only be answered with "Yes" or "No." They are inserted into special hexagonal "windows."
- **Reporter blocks** are rounded blocks that report a number or word to the program, such as the current speed or a player's name. Other blocks also have special holes of a similar shape for these.
- **C-blocks** are shaped like the letter "C" or the letter "P" lying down to rest. You can insert other commands into them, like an open mouth. They are used to repeat actions multiple times or to execute them only under a certain condition.
- **Cap blocks** are blocks that are connected only at the top. Blocks below them cannot be connected, so they are placed only at the very end of the script. For example, the "stop everything" block.

![Different types of blocks]({{ "/assets/images/scratch/main-window-blocks.png" | relative_url }})

## Command Sequence

To make something more complex, you need to understand what a command sequence is. Blocks in Scratch can be connected into a sequence, similar to a recipe. They will be executed sequentially, from top to bottom.

A command is what you want the kitten to do, and a block is the button you press to issue that command.

For example, after Scratch the kitten says hello, it might ask your name. To do this, from the blue "Sensors" group, select the "Ask What's your name? and wait" block and drag it directly under the "Say *Hello! My name is Scratch!* for *2* seconds" block so that it becomes magnetized. Then add the "Say *Hello!*" block from the purple "Appearance" group. Now go to the green "Operators" group and find the round "Merge *apple* and *banana*" block. Drag it to the workspace above the word "Hello!" in the last block. The input field with the word "Hello!" will be outlined in white. Then you can release the mouse button.

Then click on the word "apple" and replace it with "Nice to meet you," (be sure to leave a space after the comma, otherwise the words will stick together and become "Nice to meet you, Dima"). Excellent! Go to the blue "Sensors" group and take the rounded "answer" reporter block from there. Drag it to the word "banana" in the last block.

To check, click on the kitten.

![Kitten's Question]({{ "/assets/images/scratch/main-window-question.png" | relative_url }})

## Movements and Sounds

Let's try another way to launch the program - using the green flag. To do this, drag the "When Flag is Pressed" block from the yellow "Events" group to the workspace. Add to it the "Walk *10* steps" block from the blue "Movements" group. Then add the "Play Meow sound until the end" block from the purple "Sound" group and another "Walk *10* steps" block. In the last block, change the number to *-10*. It should look like this:

![Move Kitten]({{ "/assets/images/scratch/main-window-move.png" | relative_url }})

To launch the program, click the green flag above the stage. Scratch the kitten will move to the right, meow, and return.

There's another similar purple sound block in the block palette: "Turn on Meow Sound." Let's try changing the sound block in our program. To do this, detach the last block. Delete the "Play Meow Sound Until End" block. You can drag it back to the block palette to do this. Add the "Turn on Meow Sound" block. And reattach the "Walk -10 Steps" block.

![Replacing Blocks]({{ "/assets/images/scratch/main-window-replace-blocks.png" | relative_url }})

Try clicking the flag above the scene and running the program. What's changed? It looks like the kitten has stopped moving. In fact, it's still moving right and then immediately left, but it happens so quickly that we don't have time to notice. The problem is that when the program reaches the "Play the Meow sound until the end" block, it doesn't move on to the next block until the sound ends. When the program reaches the "Turn on the Meow sound" block, the sound only starts playing and the program immediately moves on to the next block without waiting.

To fix our program, take the "wait 1 second" block from the orange "Controls" group and insert it immediately after the "Turn on the Meow sound" block, so that the "move -10 steps" block moves to the end of the script.

![Fixing the program]({{ "/assets/images/scratch/main-window-move-fixed.png" | relative_url }})

Now our program works as expected again.

## Loops

What if we want Scratch the kitten to repeat these actions? Do we really have to add the same blocks multiple times?

This will certainly work, but you can use the special "repeat 10 times" C-block from the orange "Control" group. Drag it directly below the "When flag is pressed" block so that its shadow covers all the other blocks, and release the mouse button. Then, below the "go -10 steps" block, add another "wait 1 second" block.

![Loop]({{ "/assets/images/scratch/main-window-repeat.png" | relative_url }})

We can save our program to our computer using the "File" menu.

What we've learned:

- Set up your workspace: open Scratch in a browser or install it on your computer.
- Distinguish blocks by shape: use header blocks to start a program, stack blocks for actions, and special shapes for complex tasks.
- Compose algorithms: connect commands in the correct sequence so the computer executes them from top to bottom, like a recipe.
- Use loops: use C-blocks to avoid copying the same commands over and over.
- Save your work: use the "File" menu to keep your projects from getting lost.

**Star Challenge**: Try changing the number in the "Repeat 10 Times" block to 20, and in the "Go" block to 50. What will happen to the kitten? Don't be afraid to experiment; nothing can break in Scratch!
