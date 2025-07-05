 K-Safe Collision Mapper 🚄🛡️  
Efficient Point Cloud Collision Detection using K-D Trees  
_A Final Project for Advanced Data Structures & Algorithms (CSPE-43)_



 🎯 Project Summary

This project solves the real-world problem of collision detection in constrained 3D environments such as tunnels and automotive assembly lines. It implements efficient algorithms (`kd-CD`, `kd-CD-simple`, `kd-PD`, `kd-PD-fast`) to detect contact points and compute penetration depth between large-scale point cloud models.



 🔍 Core Algorithm

Implemented in C++, the core logic uses a manually constructed K-D Tree for:

- Spatial partitioning of 3D environment points
- Radius-based search to identify nearby collision candidates
- Penetration depth calculation per model point

 🔢 Key Logic in `main.cpp`:


double performCollisionDetection(Node* root, const Point& modelPoint, double searchRadius,) {
    double distance = calculateDistance(root->point, modelPoint);
    if (distance <= searchRadius) {
        // Collision Detected!
        penetrationDistance = searchRadius - distance;
    }
   
}


Each model point is tested against the environment's K-D Tree to detect:

* 📍 Colliding points
* 📏 Minimum and maximum penetration
* 📊 Average severity across all collisions

The program takes point cloud input interactively and outputs per-point collision data.

✅ Full C++ source is available in [`main.cpp`](./src/main.cpp)



 🧠 What You Learn from This Project

* How to build a K-D Tree manually (no libraries)
* Optimized traversal for 3D collision detection
* Applying DSA principles (trees, recursion, spatial search) in a real-world context
* Processing large point clouds with constrained compute



 📁 Folder Structure


K-Safe-Collision-Mapper/
├── src/
│   └── main.cpp               C++ implementation of K-D tree & collision detection
├── report/
│   └── ADSA_final_report.docx   Full documentation and analysis
└── README.md




 📈 Performance Snapshot

| Metric             | Value                              |
|  | - |
| Point cloud size   | 18.92 million (environment)        |
| Model size         | 2.5 million                        |
| Trajectory samples | 19,392                             |
| Full run time      | \~77 seconds (1.6GHz CPU)      |
| Languages used     | C++, Python (optional for viz) |



 🧑‍🎓 Academic Context

* Course: Advanced Data Structures & Algorithms (CSPE-43)
* Institution: Department of CSE
* Team Members:

  * Ajay Surya – 106122007
  * Briju Anand – 106122025
