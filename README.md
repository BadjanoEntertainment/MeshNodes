# MeshNodes Documentation

## Overview
MeshNodes is a node-based mesh editing tool. It allows for the creation, manipulation, and editing of meshes in a node-based environment, providing a visual and intuitive way to work with meshes.

## Key Components

### MeshNodes Editor
The MeshNodes editor is a custom editor that provides a visual interface for working with MeshNodes. It allows you to create and connect nodes to define complex mesh transformations. You can launch the MeshNodes editor by clicking on the `Tools` menu.

### GUISkin File
The GUISkin file located at `Assets/MeshNodes/Resources/GUISkins/EditorSkins/NodeEditorSkin.guiskin` allows you to customize the appearance of the nodes in the MeshNodes editor. You can modify this file to change the colors, fonts, and other visual properties of the nodes.

## Usage
To use MeshNodes, open the MeshNodes editor by clicking on the `Tools` menu. Before adding nodes, you first need to create a new graph. Right-click inside the node editor and choose `Graph/New`. 

Once the new graph is created, you can add nodes by right-clicking inside the node editor and choosing `New Node`, then select the node you wish to add. Connect nodes by clicking and dragging from the output of one node to the input of another. This allows you to define the transformations you want to apply to your mesh. 

You can add a graph as a node inside another graph by using the Graph Node. This allows for more complex and nested operations.

Inside the output node, there is a `Build Mesh` button. Clicking this button will add the mesh to your scene and also save a mesh file into the `MeshNodes/Database/Meshes` folder.

Please note that the MeshNodes scripts are compiled into a DLL and should only be used inside the nodes visual interface. They are not accessible for direct modification.

Each node represents a specific operation that can be performed on a 3D mesh. These operations include transformations like translation (moving), rotation, and scaling, as well as more complex operations like bending, extruding, inflating, merging, subdividing, and twisting.

Here's a brief summary of each node:

- Array: Duplicates the mesh using translation, rotation, and scaling.
- Bend: Bends the mesh using a pivot, rotation axis, and angle.
- Bevel: Bevel mesh edges and corners into a smoother mesh.
- Custom Mesh: Loads a mesh from the project into the node system.
- Extrude: Extrudes faces of the mesh.
- Instances: Instantiates meshes into the center of each face or vertex.
- Filter: Removes faces either randomly or by index or range.
- Flip Normals: Flips the normals of the mesh.
- Hook: Pull vertices from a specific position into an offset.
- Inflate: Pushes vertices along their normals.
- Merge: Merges two meshes together.
- Primitive: Creates a primitive mesh like a sphere, cylinder, cube, capsule, plane, or quad.
- Rotate: Rotates the mesh.
- Scale: Scales the mesh.
- Spherify: Morphs any mesh into a sphere shape.
- Subdivide: Divides the mesh into smaller chunks of faces.
- Taper: Scales a mesh with different intensity depending on the position in an axis.
- Translate: Moves a mesh.
- Twist: Twists a mesh using pivot, axis, and angle.
- Graph: Add another (sub)graph into your graph.
- Smooth: Smooth vertices positions using its neighbours.
- UV Transform: Adjust uv's scale, offset and rotation.
- Color: Add vertex color to your mesh.

These nodes can be connected together in a graph to create complex transformations and effects on 3D meshes.

### Custom Node

You will find a custom node sample at `/Assets/MeshNodes/Extensions/Editor/` folder, you can duplicate and rename it, and add your own math to it!

## Issue Tracking and Documentation(WIP)

Please visit https://github.com/BadjanoEntertainment/MeshNodes
