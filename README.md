# <img src="https://github.com/fini03/3D-Tetris-WebGL/blob/main/tetris-icon.png" width=30px> 3D Tetris WebGL

This is a game developed for the course "GFX - Foundations of Computer Graphics" at the University of Vienna. The objectives of this task was to create a 3D tetris game to understand 3D transforms, 3D viewing pipelines, collision detection and try out WebGL. By default the VAO_CUBE is selected which means the tetraminos are cubes.

## Usage and additional remarks
Please serve from a webserver: `python -m http.server`
For the shadow maps this [tutorial](https://xem.github.io/articles/webgl-guide-part-2.html#3b). The `unpackDepth` method and also the basic.frag shader were also taken from this tutorial. Certain shadow artifacts don't show up in the phong shading because of the [bias calculation](https://learnopengl.com/Advanced-Lighting/Shadows/Shadow-Mapping).
There is also a "cheating mode" which has been added to make testing easier. If activated (click on the checkbox) you can pause the game (gravity) and translate/rotate your object easier to the desired position. Please note that pressing 'Spacebar' won't work in this mode so you will need to unpause the game.

## 🎮 Controls
* `cw` - clockwise
* `ccw` - counter clockwise

### 👾 Game Settings
| Key                           | Description                           	      |
|-------------------------------|------------------------------------------------ |
| <kbd>P</kbd>                  | Pause / Unpause the game                        |
| <kbd>G</kbd>                  | Toggle 3D grid                         	      |
| <kbd>F</kbd>                  | Switch between Gouraud & Phong Shading          |
| <kbd>G</kbd>                  | Switch between Orthographic & Perspective View  |
| <kbd>+</kbd>                  | Zoom In                                         |
| <kbd>-</kbd>                  | Zoom Out                                        |
<br/>


### 🎥 Camera
#### Movement
| Key              | Description                                                          |
|------------------|--------------------------------------------------------------------- |
| <kbd>I</kbd>     | Rotate the camera ccw on the X-Axis around the center of the grid    |
| <kbd>K</kbd>     | Rotate the camera cw on the X-Axis around the center of the grid     |
| <kbd>J</kbd>     | Rotate the camera ccw on the Y-Axis around the center of the grid    |
| <kbd>L</kbd>     | Rotate the camera cw on the Y-Axis around the center of the grid     |
| <kbd>U</kbd>     | Rotate the camera ccw on the Z-Axis around the center of the grid    |
| <kbd>O</kbd>     | Rotate the camera cw on the Z-Axis around the center of the grid     |
<br/>

#### 🖱️ Mouse Control
| Movement              | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
| ←🖱️                   | Rotate the camera cw on the Y-Axis around the center of the grid    |
| 🖱️→                   | Rotate the camera ccw on the Y-Axis around the center of the grid   |
<br/>

## <img src="https://github.com/fini03/3D-Tetris-WebGL/blob/main/tetracube.png" width=30px> Tetracubes
#### Movement
| Key              | Description                               |
|------------------|------------------------------------------ |
| <kbd>🡅</kbd>    | Move the cube in the negative Z direction |
| <kbd>🡇</kbd>    | Move the cube in the positive Z direction |
| <kbd>🡄</kbd>    | Move the cube in the negative X direction |
| <kbd>🡆</kbd>    | Move the cube in the positive X direction |
| <kbd>Space</kbd> | Let the cube drop down                    |
<br/>

#### 😵‍💫 Rotation
| Key                           | Description                           	|
|-------------------------------|-----------------------------------------|
| <kbd>X</kbd>                  | Rotate the cube ccw around the X-Axis 	|
| <kbd>⇧</kbd> + <kbd>X</kbd> 	| Rotate the cube cw around the X-Axis  	|
| <kbd>Y</kbd>                  | Rotate the cube ccw around the Y-Axis 	|
| <kbd>⇧</kbd> + <kbd>Y</kbd>  	| Rotate the cube cw around the Y-Axis  	|
| <kbd>Z</kbd>                  | Rotate the cube ccw around the Z-Axis 	|
| <kbd>⇧</kbd> + <kbd>Z</kbd> 	| Rotate the cube cw around the Z-Axis  	|
<br/>

#### 🎭 Shapes
> Please note: if you don't switch back to tetracubes afterwards (pressing the same key), you might need to press the key `n` twice to switch to the among-us mode

| Key                           | Description                           	              |
|-------------------------------|------------------------------------------------------ |
| <kbd>B</kbd>                  | Switch to rendering cylinder instead of tetracubes 	  |
| <kbd>N</kbd>                 	| Switch to rendering among-us instead of tetracubes  	|
