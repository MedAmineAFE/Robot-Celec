# 🤖 Robot ROS Project

A modular robotics project built using **ROS (Robot Operating System)**, focused on **simulation**, **mapping**, **navigation**, and **real-world deployment** via a Raspberry Pi.

## 📁 Project Structure

```
robot_ros_project/
├── .github/workflows/          # CI workflows (e.g., ROS build tests)
├── catkin_ws/src/              # ROS workspace source
│   ├── actuator_drivers/       # Motor drivers and hardware interfacing
│   ├── sensor_drivers/         # IMU, ultrasonic, etc.
│   ├── vision_processing/      # Computer vision modules (OpenCV, YOLO)
│   ├── mapping/                # SLAM and map building (gmapping, etc.)
│   ├── localization/           # AMCL or other localization methods
│   ├── motion_planning/        # Move base, planners, costmaps
│   ├── central_control/        # Finite state machine, mission control
│   └── rosserial/              # Communication with microcontrollers
```

## 🧠 Project Goals

- 🗺️ **Mapping**: Build maps using gmapping or SLAM.
- 📍 **Localization**: Use AMCL for position estimation.
- 📦 **Motion Planning**: Plan and follow paths with `move_base`.
- 👁️ **Vision Processing**: Detect objects and colors with OpenCV.
- ⚙️ **Hardware Control**: Communicate with actuators/sensors via Arduino and ROS Serial.
- 🧠 **Autonomy**: Use a state machine to coordinate tasks.

## 💻 Development Environment

- ROS (Melodic / Noetic)
- Python 3 / C++
- Ubuntu or Raspbian (via VM for testing)
- Raspberry Pi for real-world deployment

## 🚀 How to Launch

```bash
cd robot_ros_project/catkin_ws
catkin_make
source devel/setup.bash
roslaunch central_control main_controller.launch
```

## 👥 Team Workflow

- Project hosted on **GitHub**
- Each module lives in its own ROS package
- Team members work on branches and open Pull Requests
- CI tests will validate build integrity (`ros_ci.yaml`)

## 📜 License

MIT License
