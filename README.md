## Robot Package Template

This is a GitHub template. You can make your own copy by clicking the green "Use this template" button.

It is recommended that you keep the repo/package name the same, but if you do change it, ensure you do a "Find all" using your IDE (or the built-in GitHub IDE by hitting the `.` key) and rename all instances of `my_bot` to whatever your project's name is.

Note that each directory currently has at least one file in it to ensure that git tracks the files (and, consequently, that a fresh clone has direcctories present for CMake to find). These example files can be removed if required (and the directories can be removed if `CMakeLists.txt` is adjusted accordingly).

Build:
colcon build --symlink-install

1. source /opt/ros/humble/setup.bash
2. source install/setup.bash
3. ros2 launch my_bot rsp.launch.py
4. ros2 run joint_state_publisher_gui joint_state_publisher_gui
5. ros2 run rviz2 rviz2

1. ros2 launch my_bot rsp.launch.py use_sim_time:=true
2. ros2 run gazebo_ros spawn_entity.py -topic robot_description -entity bot_name
3. ros2 launch gazebo_ros gazebo.launch.py