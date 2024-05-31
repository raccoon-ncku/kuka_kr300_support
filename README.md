# KR 300 R2500 ultra Support Package

## Geometry

### Collision Model
The collision meshes are generated from the CAD model of the robot. This package utilizes meshlab to convert visual meshes to collision meshes with the following steps:

1. Open the visual mesh in meshlab
2. Filters -> Remeshing, Simplification and Reconstruction -> Convex Hull
3. Filters -> Remeshing, Simplification and Reconstruction -> Simplication: Clustering Decimation: tune the percentage to get the desired level of simplification, idealy 100-200 faces per link.
4. Filters -> Remeshing, Simplification and Reconstruction -> Convex Hull
5. File -> Export Mesh As... -> Select the file type as STL and save the file in binary format

# URDF
```sh
rosrun xacro xacro -o kr300r2500pro.urdf kr300r2500pro.xacro
```

## Known Issues
- The actual name of this robot is KR 300 R2500 ultra, yet it is named as `kr300r2500pro` in the package.
- Generating `.dae` files from Rhino 8 yeilds self-closing tags. Also rviz, moveit can't visualize the model even after solving the self-closing tags issue. Right now, the model is still using the `.stl` files for visualization.