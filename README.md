# Asynchronous AGV Warehouse Simulator

A high-performance, hybrid Python/C++20 simulation environment for Automated Guided Vehicles (AGVs) navigating a dynamic warehouse grid. This project focuses on real-time determinism, efficient sensor data handling, and fail-safe safety mechanisms in autonomous logistics.

## Key Features
* **Hybrid Architecture:** Combines Python's flexibility for grid orchestration with C++20's raw performance for critical control loops.
* **Asynchronous Stream Isolation:** Utilizes the ROS 2 `MultiThreadedExecutor` to process high-frequency sensor streams independently, preventing telemetry bottlenecks.
* **Deterministic Safety Watchdog:** Leverages C++20 concurrency primitives (`std::jthread`, `std::stop_token`) to build a low-latency, interrupt-driven safety system that prevents collisions.

## System Architecture
* **Simulation Core:** ROS 2 (Humble/Iron)
* **Language Specs:** C++20, Python 3.10+
* **Concurrency:** `std::jthread`, ROS 2 MultiThreadedExecutor, Mutexes/Condition Variables

## Getting Started

### Prerequisites
* ROS 2 installed (Humble or later recommended)
* colcon build tool
* C++20 compatible compiler (GCC 11+ or Clang 13+)

### Installation & Run
1. Clone the repository into your ROS 2 workspace:
   ```bash
   cd ~/ros2_ws/src
   git clone [https://github.com/yourusername/agv-warehouse-sim.git](https://github.com/yourusername/agv-warehouse-sim.git)
