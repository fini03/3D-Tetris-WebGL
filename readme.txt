-- claim section --

All tasks T1, T2, T3, T4, T5, T6, T7, T8 as well as B1, B3 (some parts), B4 have been fully implemented.

By default the VAO_CUBE is selected which means the tetraminos are cubes. To switch to cylinders (VAO_CYLINDER) you can press the key 'b'.

Additionally, a VAO_AMONGUS has been implemented (as part of B3), which will render the tetraminos to among us characters. To switch to this mode you can press the key 'n', pressing the key again will go back to VAO_CUBE. Please note that if you don't switch back to VAO_CUBE afterwards, you might need to press the key 'n' twice to get to the VAO_AMONGUS mode. For B3, background-music ("Play Audio" button to play the music and "Stop Audio" to stop the music) as well as sound effects when clearing a row or a shape falls down has been implemented. These were accounted for "anything creative you can think of". Also, the shape changes its color when colliding (textures stay the same). Since the color is picked randomly there is a slight chance that the new selected color is the same. For B3 "at random every 5th block or so should be transparent" has been added as well.

In B1 instead of displaying a new window a button ("Restart Game") has been added, so you can restart the game at any time.

For B4 shadow maps were used because shadow maps are based. Only the shadow of the current object is being rendered. The ground plane alpha-value has been set to 0 and only the shadow is displayed. The shadow of the current object is drawn on other underlying shapes. Backfaces are culled for shadow maps in order to not draw erronous self-shadows, so shadows will only be correct for closed-surface objects.

Also for the shadow maps this tutorial has been used: https://xem.github.io/articles/webgl-guide-part-2.html#3b. The `unpackDepth` method and also the basic.frag shader were also taken from this tutorial. Certain shadow artifacts don't show up in the phong shading because of the bias calculation. The used bias formula (in phong shading) was taken from: https://learnopengl.com/Advanced-Lighting/Shadows/Shadow-Mapping.

There is also a "cheating mode". This mode has been added to make testing easier. If activated (click on the checkbox) you can pause the game (gravity) and translate/rotate your object easier to the desired position. Please note that pressing 'Spacebar' won't work in this mode so you will need to unpause the game.

-- tested environments --

The assignment was created on endeavourOS (version: 6.1.8-arch1-1, graphic card: Intel Corporation HD Graphics 620 (rev 02), browser: Mozilla Firefox 109.0) tested on arch linux (version: 6.2.2-arch1-1, graphic card: Intel Corporation UHD Graphics 620 (rev 07), browser: Mozilla Firefox 110.0.1 and Chromium 111.0.5563.64). It was also tested on Windows 11 Pro with Firefox (Firefox version: 92.0, graphic card: Intel Corporation HD Graphics 620 (rev 02)).

-- additional and general remarks --

Please serve from a webserver:
    - python -m http.server

Initial page: index.html

For the assignment only the vertex array object from WebGL2 was used. It was chosen to simplify the vertex data management (put all of the necessary vertex data for the application into a single object) and for better code organization (using the VAO to store all the vertex attribute bindings). The rest of the code is still written according to WebGL standards.
