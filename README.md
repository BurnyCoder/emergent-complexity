# Emergent complexity

Interactive generative art visualization where particles move based on the [Clifford Attractor](https://en.wikipedia.org/wiki/Clifford_attractor) and user-adjustable parameters for particle count, trail opacity, repulsion strength/radius, color influence, density threshold, and anti-cluster force, forming complex patterns on a canvas. Made with HTML with Canvas API, Tailwind CSS, JavaScript.

![image](https://github.com/user-attachments/assets/d903e76f-bc08-4da2-87ae-5ec306d41d89)

Video: https://youtu.be/bXrRpF_-TTM

## How to Run

Open emergent-complexity.html file

## Features

* **Generative Art:** Creates dynamic and complex visual patterns based on mathematical rules and particle interactions.
* **Clifford Attractor:** Utilizes the Clifford Attractor equations to guide the target positions of particles, creating characteristic fractal-like structures.
* **Particle System:** Simulates numerous individual particles moving on the canvas.
* **Interactive Controls:** Allows real-time adjustment of various simulation parameters via UI sliders:
    * Number of Particles
    * Trail Opacity (how quickly old positions fade)
    * Particle Repulsion Strength & Radius
    * Color Influence Strength (how much nearby particles affect each other's hue)
    * Density Threshold & Anti-Cluster Force (to prevent excessive clumping)
* **Color Blending:** Particles gradually change their color (hue) based on the colors of their neighbors.
* **Anti-Clustering:** Implements a force that pushes particles away from areas that become too dense.

## Controls

The control panel in the top-left corner allows you to manipulate the simulation:

* **Particles:** Adjusts the total number of particles simulated. *Changing this value will reset the simulation.*
* **Trail Opacity:** Controls the alpha value of the background fill on each frame. Lower values result in longer particle trails; higher values result in shorter trails.
* **Repulsion:** Sets the strength of the force pushing particles away from each other when they are within the repulsion radius.
* **Repulsion Radius:** Defines the distance within which particles exert repulsive forces on each other.
* **Color Influence:** Determines how strongly a particle's target hue is influenced by the hues of its neighbors.
* **Density Threshold:** Sets the minimum number of neighbors within the `DENSITY_CHECK_RADIUS` required to trigger the anti-cluster force.
* **Anti-Cluster Force:** Controls the strength of the force pushing particles away from the center of dense clusters.
* **Reset Simulation Button:** Restarts the simulation with the current parameter settings but new random constants for the Clifford Attractor and new initial particle positions/velocities.

## Potential Improvements

* Add more attractor types (e.g., De Jong, Peter de Jong).
* Implement mouse interaction (e.g., attract/repel particles).
* Optimize performance for a larger number of particles.
* Add functionality to save the current canvas state as an image.
* Explore different color mapping strategies.
