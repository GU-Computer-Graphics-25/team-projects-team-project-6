# Team: Team Project 6
## See the project live at: 
### <a href="https://gu-computer-graphics-25.github.io/team-projects-team-project-6/" target="_blank">Project Demonstration</a>

## Project Scene Description/Summary
This scene we have implemented is inspired by the toy story aliens. We have created and positioned three “toy story aliens” in the middle of the scene. Each alien has an oval shaped head and body, with arms, circular hands, rounded feet, a mouth, three alien eyes, an antenna, ears, and a belt and scarf to make the alien body look like it is wearing a space suit. Around these aliens we have added a toy rocket ship, toy blocks, and a hanging mobile of planets. When "g" is pressed, the animation begins, so the planet mobile spins and the toy blocks spin in place while the aliens move in a circular path around the rocket ship. The scene is lit with a spotlight above the scene to make it appear "glowy".

## Features Demonstrated

The following are features that are demonstrated in this project scene:

- animation
    - In the scene, when "g" is pressed 3 animations start:
        1) the toy blocks spin/rotate in place
        2) the planets mobile above the aliens spins
        3) the three aliens move in a circular path
    - Then, so stop the animation the user presses "s"
        - the aliens go back to their starting position 
- modeling, particularly hierarchial
    - alien is a composite object containing a head, body, arms, and feet
        - the head has ears, eyes, a mouth, and an antenna
        - the body has a belt and scarf to mimic a space suit
        - the arms have circle hands
    - rocket ship is a composite object of the rocket ship body, the three fins, and the window
    - planet mobile is a composite object with the north/south/east/west planets, the frame (cylinder "poles"), and lines to connect the planets
    - toy blocks are a composite object because the three blocks are all added to the container object that groups them together
- curved lines or surfaces
    - body of the rocket ship is a custom geometry that was made using a custom Bezier surface generation function (from Mads) that creates a radially symmetric surface around the y-axis given an array of points
    - path the aliens take around the ship is mapped by a Bezier curve
- material, lighting and shading
    - using Three.js's MeshPhongMaterial and lighting objects to make the alien's glossy and the space ship's window shiny/reflective
    - alien's space suit uses lambert material to appear closer to cloth
    - alien skin and rocket ship use "standard"/ "basic" material to look more matte
    - ambient light source to provide even, general lighting to the scene
    - directional light and a spotlight to create the glowy effect where the aliens are "spotlighted"
- changing camera position or shape
    - use Three.js PerspectiveCamera object to render scene's camera
        - adjusted camera's position, up, and lookAt values so when the scene renders, the camera angle is facing the aliens so we can see their faces 
        - camera is up and slightly to the right so we can see the gray rocket ship behind the aliens too
        - orbit controls also enabled to you can click and drag on the scene to get different camera angles
- textures and texture-mapping
    - textures were mapped to the toy blocks to make them look like wooden blocks
    - each planet has a single planet texture 

## Resources Used and/or Referenced
The following were used in some manner to create the project scene.
- [Three.js documentation and examples](https://threejs.org/docs/index.html)
    - note any specific relevant information on how this was explicitly used in your project
- [Learn Three.js - Fourth Edition](https://www.packtpub.com/product/learn-threejs-fourth-edition/9781803233871)
    - note any specific relevant information on how this was explicitly used in your project
- [Traffic Run Game](https://codepen.io/HunorMarton/pen/ExNzWqm)
    - Some random example - used ABC, motivated by XYZ - note any specific relevant information on how this was explicitly used in your project