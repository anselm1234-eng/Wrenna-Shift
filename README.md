# Wrenna-Shift: HTML5 Sliding Puzzle Maker

A modern, lightweight implementation of the classic sliding puzzle mini-game, built entirely with HTML DOM elements. No Canvas or third-party libraries are required. 

Created and maintained by **Anselm Wrenna**.

When shuffling the picture, the engine uses natural mixing by moving a free slot rather than random slot replacement. This guarantees that the puzzle is always solvable. 

By solving the puzzle, you can move multiple blocks in a column and row in a single move. The engine supports GamePad and keyboard controls. 

The engine code is highly flexible, has many customization settings, and can be seamlessly integrated into any web page or web app.

> Editor: https://anselm1234-eng.github.io/Wrenna-Shift/

> Demo: https://anselm1234-eng.github.io/Wrenna-Shift/example.html

## Structure

To use the engine, create a `div` element with the ID `fifteen` and add a configuration object. The script will handle the rest. It's simple to drop into your web page.

```html
<html>
    <head>
        <title>Wrenna-Shift</title>
    </head>
    <body>
        <div id='fifteen'></div> <!-- Element where the game will take place -->
        <script>
        var setup={
             puzzle_fifteen:{
                diff:300,           // Number of movements of the slots for shuffling pictures
                size:[512,640],     // Element size "fifteen" in pixels only
                grid:[3,3],         // The number of squares in the height and width of the picture
                fill:true,          // Stretching the area with the game to fit the element (recommended for fullscreen)
                number:true,        // Slot sequence number
                art:{
                    url:"art.jpg",  // Path to the picture (supports most browser formats, gif, and svg)
                    ratio:false     // Enlarge the picture in height or width
                },
                // optional elements
                time:"0.1",         // Block move animation time
                style:"border-radius:12px;", // Style for puzzle square
                emptySlot:[1],      // Empty square number, defaults to the lower right quadrant.
                keyBoard:true,      // Control using the keys on the keyboard
                gamePad:true        // Control using the joystick on the Gamepad
             }
        }
        </script>
        <script src="wrenna_shift.js"></script> <!-- Path to the rebranded engine file -->
    </body>
</html>

Editor / Demo
Upload your own image, set the parameters, and generate an HTML file with the game and your image. You can use the resulting file on your website, directly on your device, or modify it further to run your own custom scripts when the game finishes.

Play the online maker here: https://anselm1234-eng.github.io/Wrenna-Shift/

Editor Features:
Automatic style adaptation based on image dimensions

Proportional division of an image into blocks

Building / exporting HTML files with the game

Moving multiple blocks in one move

Drag and Drop image upload