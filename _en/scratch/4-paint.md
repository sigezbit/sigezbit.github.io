---
layout: post
title: "4. Paint app"
topic_slug: "scratch"
order: 4
---

It's time to dive deeper into the "Pen" extension. We already used it to draw a rocket trail earlier. Now let's create a full-fledged drawing program! First, create a new project. Then click the "Add Extension" button in the lower left corner and select the "Pen" extension.

For our Paint app, we won't need the cat sprite. Delete it, and add the "Pencil" sprite from the sprite library instead. Change its size to *30* in the input field below the stage, then switch to the "Code" tab.

First, let's make the pencil follow the mouse pointer. Add a "when flag clicked" header block and attach a purple "go to front layer" block. This ensures the pencil always stays on top of any other sprites. Next, add an orange "forever" block, and place a blue "go to random position" block inside, changing "random position" to "mouse-pointer".

Now, when you run the program, the pencil follows your mouse, but it doesn't draw anything yet. To start drawing, add another "when flag clicked" block and connect blocks from the "Pen" extension: "erase all" and "set pen size to 1". Change *1* to *5* so the line is thicker. After that, add an orange "forever" block and place an "if ... then ... else" block inside (it looks like the letter "E"). Into the hexagonal condition slot, insert the light blue "mouse down?" sensing block. In the upper part of the block, insert the "pen down" extension block, and in the lower part, insert "pen up". This block works like a toggle switch: when the mouse button is pressed, we draw; when it's released, we just move the pencil.

![Pencil code]({{ "/assets/images/scratch/paint-draw.png" | relative_url }})

Run the program and see what we've got. For some reason, the trail isn't drawn from the pencil tip, but from its middle! That's because the "Pen" extension always draws from the center of a sprite. To make the pencil draw properly, switch to the "Costumes" tab. In the center of the canvas is a small gray crosshair—this is the sprite's "drawing point" (center point). Select the entire pencil drawing and drag it so the tip of the lead points directly at this crosshair.

![Centering pencil]({{ "/assets/images/scratch/paint-pencil-center.png" | relative_url }})

Let's add a button to clear the drawing. Add the "Button 3" sprite from the sprite library, change its size to *50*, move it to any corner so it doesn't get in the way of drawing, and switch to the "Code" tab. Add a "when this sprite clicked" header block and attach the pen block "erase all".

![Clear button code]({{ "/assets/images/scratch/paint-clear.png" | relative_url }})

> Notice that if you run the program in "Small Stage" or "Large Stage" mode (the buttons above the stage), you can drag the clear button around with your mouse, but if you switch to "Fullscreen" mode, you cannot.

The "Small Stage" and "Large Stage" modes are working/editing modes. In these modes, sprites can be moved with the mouse even if you use the sensing block "set drag mode not draggable". Conversely, to allow a sprite to be dragged in "Fullscreen" mode, you must explicitly use the sensing block "set drag mode draggable".

In addition, projects sometimes run slightly smoother in fullscreen mode (especially on older or slower computers) because the browser doesn't have to constantly redraw the yellow glow around running blocks in the code workspace.

Now let's add a color palette so we can choose drawing colors. We'll use the same kind of buttons. Right-click the "Button 3" sprite and select "Duplicate". Then go to the "Costumes" tab and select the "Fill" tool (the paint bucket icon). Click the fill color, set Color to *0*, and set Saturation and Brightness to *100*, then click on the button illustration. You'll get a red button! In the same way, add a yellow button (Color *16*), green (*32*), blue (*64*), and purple (*80*). Arrange the buttons along the edges of the stage so they don't block your drawing area.

Select the red button sprite and switch to the "Code" tab. Add a "when this sprite clicked" block and attach a "broadcast message1" block. Create a new message called "Red". Add the same code for the other color buttons, broadcasting their respective color names.

![Red button code]({{ "/assets/images/scratch/paint-color.png" | relative_url }})

Now we need to add code to the pencil so it responds to these broadcast messages. Select the pencil sprite and go to the "Code" tab. Add a "when I receive Red" block, attach a "set pen color to ..." block, and set Color to *0*, Saturation and Brightness to *100*—just like the button fill. Add similar blocks for each of the other colors with their corresponding color numbers.

![Complete program]({{ "/assets/images/scratch/paint-result.png" | relative_url }})

Now you can start the program and draw!

What we've learned:

- Draw multicolored lines and clear the canvas with a single command.
- Bring a sprite to the front layer so it always stays visible above other sprites.
- Use multiple buttons to create a real graphic drawing tool.
- Understand stage modes: how fullscreen mode affects sprite dragging and performance.

**Starred tasks**:

- Add buttons to increase and decrease pen size using the "change pen size by ..." block.
- Add an "Eraser" button to your program. An eraser is just like the pencil, but it draws in the background color (white) and has a very large pen size.
