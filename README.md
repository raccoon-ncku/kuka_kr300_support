# KR 300 R2500 ultra Support Package

## Geometry

### Collision Model
The collision meshes are generated from the CAD model of the robot. This package utilizes meshlab to convert visual meshes to collision meshes with the following steps:

1. Open the visual mesh in meshlab
2. Filters -> Remeshing, Simplification and Reconstruction -> Convex Hull
3. Filters -> Remeshing, Simplification and Reconstruction -> Simplication: Clustering Decimation: tune the percentage to get the desired level of simplification, idealy 100-200 faces per link.
4. Filters -> Remeshing, Simplification and Reconstruction -> Convex Hull
5. File -> Export Mesh As... -> Select the file type as STL and save the file in binary format