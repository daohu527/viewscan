## Vehicle and sensor layout
We obtain the sensor layout through vehicle size and sensor external parameters.
- vehicle size
- sensor external parameters

## FOV
We describe the vehicle's fov through an octree. For lidar and cameras, we can adjust the size of the box to obtain finer resolution.
For example, the angle between lidar rays may cause missed detections.
The minimum pixel resolution of the camera can also cause missed detections.

This can all be represented using an occupancy grid.

## collision detection
We use ray cast for collision detection. Thanks to the octree, we can reduce the calculation range to increase the processing speed.

## Solutions
1. Obtain the sensor position and orientation through the vehicle size and sensor external parameters.
2. Build octree
3. Determine whether there is a collision through rays, and the collision will not be displayed.
4. Display occupied network in the front three.js

#### collision detection
1. lidar use raycast
2. camera uses 3D box projection to 2D to determine whether it is within the field of view.
