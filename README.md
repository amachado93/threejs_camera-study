# Camera study

I have been making 3D models for a few months, but never took the time to understand the differences between perspective and orthographic cameras and the their use cases.

The sketch I made using Three.js quickly demonstrates this difference.  I may come back at a later time and use a more interesting mesh.

## Perspective Camera
The perspecitve camera is useful for capturing how things look in the real world.  In other words, objects that are closer to the camera appear to be larger than those farther away from the camera. It is the most common projection mode used for rendering a 3D scene.

To implement this camera type in your Three.js scene, you'll need to use the `PerspectiveCamera()` constructor.  This constructor takes four arguments to define the camera's frustum.

The four arguments are:
- fov: Camera frustum vertical field of view.
- aspect: Camera frustum aspect ratio.
- near: Camera frustum near plane.
- far: Camera frustum far plane.

### Code example
Create your perspective camera with - ``const camera = new THREE.PerspectiveCamera(75, 1, 0.1, 10)``
And be sure to add your camera to your scene with - ``scene.add(camera)``

## Orthographic Camera
The orthographic camera is useful for communicating dimensions unambiguously.  An object's size in the rendered image stays constant regardless of its distance from the camera.  This can be useful for rendering 2D scenes and UI elements, amongst other things.

To implement this camera type in your Three.js scene, you'll need to use the `OrthographicCamera()` constructor.  This constructor takes six arguments to define the camera's frustum.

The six arguments are:
- left: Camera frustum left plane.
- right: Camera frustum right plane.
- top: Camera frustum top plane.
- bottom: Camera frustum bottom plane.
- near: Camera frustum near plane.
- far: Camera frustum far plane.

### Code example
Create your orthographic camera with -``const camera = new THREE.OrthographicCamera(-1, 1, 1, -1, 0.1, 10)``
Once again, be sure to add your camera to your scene with - ``scene.add(camera)``
