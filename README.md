# ROS2-Action
This ROS2 package includes a simple service, a custom service, and custom message definitions. It demonstrates how to create, build, and use custom interfaces in ROS2, enabling communication between nodes through user-defined message and service types for flexible and efficient robotic applications.

---

## Overview

- **Simple Service:** Demonstrates a basic request-response service communication.
- **Custom Service:** Defines a user-created `.srv` file for custom service functionality.
- **Custom Message:** Includes custom `.msg` types for flexible data exchange between ROS2 nodes.

---

## Features

- Create and build custom messages and services in ROS2.
- Implement client-server communication using both standard and custom interfaces.
- Learn interface generation workflow (`.msg`, `.srv`).
- Demonstrates practical ROS2 node interaction with real-time responses.

---

## Build Instructions

### Source ROS2 Environment
```bash
source /opt/ros/humble/setup.bash
```

### Clone Repository
```bash
git clone https://github.com/yashbhaskar/ROS2-Service.git
```

### Change Directory
```bash
cd ros_ws
```

### Build the Package
```bash
colcon build --packages-select simple_service_pkg custom_service_pkg 
source install/setup.bash
```

### Launch Simple Service Server
```bash
ros2 run simple_service_pkg service.py
```

### Launch Simple Service Server
```bash
ros2 run simple_service_pkg client.py 5 10
```

### Launch Custom Service Server
```bash
ros2 run custom_service_pkg add_three_ints_server.py
```

### Launch Simple Service Server
```bash
ros2 run custom_service_pkg add_three_client.py 5 10 20
```

### OR Call Service
```bash
ros2 service call /add_three_ints custom_service_pkg/srv/AddThreeInts "{a: 5, b: 10, c: 20}"
```

---

## ✉️ Contact

📧 Yash Bhaskar – ybbhaskar19@gmail.com
📌 GitHub: https://github.com/yashbhaskar
