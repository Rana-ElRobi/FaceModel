# FaceModel
In this repo you are provided with a 3D model of a human face (face.vtk) and texture image (face.ppm). This code is required to load the textured model in a lighted scene, perform smooth Gouraud shading, manipulate the model, the lights and the camera..
# Requirements:
1. Scene setup
	Draw horizontal plane
	Draw a cube over the plane
  Insert 2 Omni light sources in different positions above the plane
2. Model loading
	 Read the VTK and the PPM files
	 Draw the textured face model exactly above the cube
3. Smooth shading
	 Produce smooth (Gouraud ‐> Average of normals around polygon) shading for visualizing a polygonal model of a face with texture mapping applied
4. Model manipulation:
	 Assign Keyboard shortcuts to move the loaded model in 3 axes back and forth
5. Light Control
 	Assign Keyboard shortcut keys for enabling/disabling each light source
6. Camera Manipulation: (using mouse)
	 Rotation
	 Zooming
	 Panning
7. visualize normal vectors at each point in the modelVTK File

# The (face.vtk) consists of following sections:
Header: file info

POINTS: number of points (number of vertices of the surface model) and point data type to
indicate the start of the vertex data. Each of the following lines contains the x, y and z world‐
coordinates for each vertex as floating point numbers.

POLYGONS: the number of polygons and the size of the cell list for all polygons. Each of the
following lines contains the number of vertices forming the polygon, followed by the indices of
the vertices which form the polygon.

POINT_DATA: followed by the number of points with texture coordinates.

TEXTURE_COORDINATES: to indicate the start of the texture data and some misc. information.
After that follow lines containing the x and y texture coordinates for each vertex as floating
point numbers. The order of the texture coordinates is the same as the order of the vertices.

# PPM File:
For texture mapping, the (face.ppm) is a 512x512 texture map of the face model. The texture map is
represented as PPM file with a short ascii header followed by the R (red), G (green) and B (blue)
components for each pixel as a separate unsigned byte.
