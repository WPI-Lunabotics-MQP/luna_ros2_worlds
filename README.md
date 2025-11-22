# luna_ros2_worlds
Updated luna_ros world files for Gazebo Harmonic + example launch files.

## File Structure
Overall file structure of this package:
```
luna_ros2_worlds/
├── launch/
│   └── arena_b.launch.py
├── models/
│   ├── arena_b
│   ├── rock_a
│   ├── rock_b
│   └── rock_c
├── worlds/
│   └── arena_b.sdf
├── CMakeLists.txt
├── package.xml
└── resources.txt
```

The file structure for each individual model inside the model folder is as shown:
```
models/
└── model-name/
    ├── meshes/
    │   └── cad-of-the-model.stl
    ├── model.config
    └── model.sdf
```

## `package.xml` notes
most important thing to remember are the three gazebo resource path lines near the end of the xml file:

```xml
  <export>
    <build_type>ament_cmake</build_type>
    <gazebo_ros gazebo_model_path="${prefix}/models"/>
    <gazebo_ros gazebo_model_path="${prefix}/worlds"/>
    <gazebo_ros gazebo_model_path="${prefix}"/>
  </export>
```

## Gazebo Sim Resources
- [Gazebo Harmonic Documentation](https://gazebosim.org/docs/harmonic/getstarted)</br>
- [Simulation Description Format (SDF)](http://sdformat.org) </br>
