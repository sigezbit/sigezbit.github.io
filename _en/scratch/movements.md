---
layout: post
title: "Sprite movements"
topic_slug: "scratch"
order: 4
---

Let's talk about sprite coordinates. These are two numbers we use to tell the computer exactly where to position the character.

It's like playing Battleship. We call the first number X, which indicates the horizontal position (left-right), and the second, Y, which indicates the vertical position (up-down). At the very center of the scene, both numbers are zero: X: 0, Y: 0. To position the sprite to the right, you need to increase X, and to position it to the left, you need to decrease it. Similarly, vertically: to raise the sprite, you need to increase Y, and to lower it, you need to decrease Y.

> If a number becomes less than zero, a minus sign appears in front of it—just like a thermometer in freezing temperatures!

You can specify numbers from -240 to 240 for the X coordinate, and from -180 to 180 for the Y coordinate. For example, if we want to position the sprite in the upper right corner, we would specify X = 240 and Y = 180, and if we want to position it in the lower left corner, we would specify X = -240 and Y = -180.

You can set the character's position using the "go to x: 0 y: 0," "set x to 0," or "set y to 0" blocks, as well as in special input fields directly below the scene. Note: if you move the sprite around the scene with the mouse, the numbers in these fields will change automatically.

To make it easier to navigate, Scratch has a special background with a coordinate grid. It's called the "Xy-grid."

![Coordinate grid]({{ "/assets/images/scratch/movements-xy-grid.png" | relative_url }})

Let's create a new project, remove the Scratch kitten sprite, and replace it with the "Rocketship" rocket sprite. Then we'll add a background with "Stars" suitable for space travel.

Select the rocket sprite and click the "Direction" input field below the scene. A small window will open where you can change its direction. Try turning the arrow. The rocket will follow it. Below the arrow are three important buttons that change the rotation method:

- "Circle" (circular arrow) - the sprite rotates freely in all directions. - "Left/Right" (two arrows pointing in opposite directions) - the sprite rotates to the right if the arrow is in the right half of the circle, and flips from right to left if the arrow is in the left half of the circle.
- "Don't Rotate" (a circle with a line through it) - the sprite always faces the same direction, no matter which way we turn the arrow.

For our game, we'll select the "Circle" mode so the rocket rotates. But look! Right now, the rocket isn't pointing in the same direction as the arrow. Let's fix that. To do this, go to the "Costumes" tab in the upper left corner of the window.

![Sprite Direction]({{ "/assets/images/scratch/movements-rotate.png" | relative_url }})

Our costume isn't simple: it's made up of the rocket itself and clouds of smoke. To rotate them together, you need to:

- Frame the drawing: Left-click and drag the drawing to the opposite corner of the rocket. A blue rectangle will appear. Align the entire rocket and smoke within it.
- Rotate the rocket: A curved arrow should appear at the bottom. Grab it with your mouse and rotate the drawing so the rocket is pointing directly to the right.

When rotating the rocket, try to align its center with the small target (crosshair) in the middle of the drawing screen. If you don't get it right the first time, simply click the back arrow above the drawing, and everything will return to normal.

![Sprite Fix]({{ "/assets/images/scratch/movements-rotate-costume.png" | relative_url }})

Now the rocket is pointed correctly. Let's write a program to make it fly. Go to the "Code" tab. Add a yellow header block called "When flag is pressed," followed by a blue block called "Go to x, y," and set both coordinates to 0. Next, add a "Turn in direction" block and set the value to 45 so the rocket flies nicely, diagonally. Next, add an orange "Repeat forever" block and insert blue blocks called "Go 10 steps" and "If touches edge, bounce."

Let's add blocks to control the rocket. Start with the yellow block called "When spacebar is pressed." Instead of the spacebar, select "Right Arrow" and attach a blue block called "Rotate clockwise 15 degrees." Then add another block called "When spacebar is pressed," but select "Left Arrow" and attach a block called "Rotate counterclockwise 15 degrees." It should look like this:

![Rocket Code]({{ "/assets/images/scratch/movements-rocket-code.png" | relative_url }})

Let's click the flag above the stage and see what we've got. The rocket flies, bounces off the edges of the stage, and turns if you press the left and right arrows.

> Notice that when the program is running, the blocks that are currently running are highlighted with a yellow outline. This is very convenient! If a script is "glowing" yellow, it means the computer is executing those commands. As soon as you click the red "Stop" circle, the glow will disappear.

## Adding Extensions

Scratch has special extensions (add-ons) that add new blocks and capabilities. For example, the "Music" extension allows you to create music and sounds, while the "Pen" extension allows you to draw on the scene. To add an extension, click the purple button with a white plus sign with blocks in the lower left corner.

![Extension Button]({{ "/assets/images/scratch/movements-extensions-button.png" | relative_url }})

The extension gallery will open. Select the "Pen" extension, and another block group will be added below the main groups of blocks, indicated by different colored circles.

![Extension Gallery]({{ "/assets/images/scratch/movements-extensions.png" | relative_url }})

With this extension, we can make our rocket leave a trail. To do this, add a yellow "When Spacebar is Pressed" block, replace the "spacebar" with a "down arrow," and attach a "lower pen" block from the new group. Add another "When Spacebar is Pressed" block, replace the "spacebar" with an "up arrow," and attach a "raise pen" block to it. Now, when you press the down arrow, the rocket will start leaving a trail, and when you press the up arrow, it will stop.

You can also change the trail color. Add another "When Spacebar is Pressed" block and attach a "change pen color to 10" block to it. And to remove all trails, add another "When Spacebar is Pressed" block, replace the "spacebar" with "0," and attach a "erase all" block to it.

In Scratch, each color has a number. When we change the color to 10, we simply move on to the next shade of the rainbow.

![Drawing code]({{ "/assets/images/scratch/movements-pen.png" | relative_url }})

Great! Run the program and see what patterns our rocket can draw!

> Above the stage on the right are three buttons: "Small Stage," "Large Stage," and "Fullscreen." Use them to change the stage's size.

What we've learned:

- Specify sprite coordinates and change its position on the stage.
- Choose a sprite rotation method and adjust its direction.
- Create programs with moving sprites and change direction using the arrow keys.
- Add extensions and use new blocks to draw on the stage.

**Starred task**: See what other blocks are available in the "Pen" extension. Think about how they could be applied in our project.
