A tool for quickly converting NURBS to triangular or quadrilateral meshes.

Generating 200,000 meshes takes only 200 milliseconds.

The effect is as follows：

![image](https://github.com/GridGeneration/AutoMeshGeneration/blob/main/data/triangle_mesh.png)
![image](https://github.com/GridGeneration/AutoMeshGeneration/blob/main/data/tri-quad_mesh.png)
![image](https://github.com/GridGeneration/AutoMeshGeneration/blob/main/data/BasicVersionAlgorithm)
![image](https://github.com/GridGeneration/AutoMeshGeneration/blob/main/data/cartesian.png)

How to use:

      AutoMesh inputcad outmesh {-s||-m||-q} [len_size] [angle_size]
	  
      inputcad: iges,ige,step,stp file
	  
       outmesh: stl,obj while using -q must be obj
	   
  {-s||-m||-q}: -s generation all mesh,-m generation split mesh,-q generation quad mesh
  
[len_size] [angle_size]  control mesh size

eg:

		AutoMesh "Rocket engine.step" "Rocket engine.stl" -s
		
		AutoMesh "Rocket engine.step" "Rocket engine.stl" -s 0.06
		
		AutoMesh "Rocket engine.step" "Rocket engine.stl" -s 0.06  0.175
		
		AutoMesh "Rocket engine.step" "Rocket engine.stl" -m
		
		AutoMesh "Rocket engine.step" "Rocket engine.stl" -m 0.06
		
		AutoMesh "Rocket engine.step" "Rocket engine.stl" -m 0.06  0.175
		
		AutoMesh "Rocket engine.step" "Rocket engine.obj" -q
		
		AutoMesh "Rocket engine.step" "Rocket engine.obj" -q 0.06
		
		AutoMesh "Rocket engine.step" "Rocket engine.obj" -q 0.06  0.175
		


