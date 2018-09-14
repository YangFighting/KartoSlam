代码介绍 基于开源的KartoSlam，机器人为启Turtlebot2,激光雷达为rplidar A2,添加内容为将定位坐标通过蓝牙串口传到手机

运行步骤

上网本新开端口，打开roscore roscore

上网本新开端口，启动turtlebot roslaunch turtlebot_bringup minimal.launch

上网本新开端口，启动karto,用于构建地图 roslaunch turtlebot_navigation rplidar_karto_demo.launch

—————————————————————————————————————————————————— 遥控turtlebot（以下二选一） 新终端设置设备并启动游戏杆遥控支持 rosparam set /joystick/dev "/dev/input/js0" roslaunch turtlebot_teleop xbox360_teleop.launch

工作机或上网本新开端口，启动键盘操作Turtlebot roslaunch turtlebot_teleop keyboard_teleop.launch ——————————————————————————————————————————————————

工作机或上网本新开端口，启动rviz，实时查看建图情况 roslaunch turtlebot_rviz_launchers view_navigation.launch

—————————————————————————————————————————————————

上网本新开端口，启动蓝牙传输 rosrun slam_karto Pos2bluetooth
