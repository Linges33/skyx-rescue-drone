# SKY-X: Autonomous AI-Powered Search and Rescue Drone

SKY-X is an autonomous drone concept that supports rescue teams after disasters such as earthquakes, building collapses, floods and fires. It detects possible victims using RGB and thermal sensing, estimates their priority, replans its search mission, and reports locations and alerts to a ground-station operator.

## Key features
- RGB + thermal sensing for victim detection
- Distance sensing for obstacle awareness
- Onboard edge AI for detection and assessment
- Dynamic victim priority scoring
- Autonomous navigation using ROS 2 and PX4
- Dynamic mission replanning
- Ground-station monitoring (video, telemetry, victim locations, priorities, alerts, coverage)
- Operator override, geofencing and failsafe controls

## Proposed system
RGB camera, thermal camera and distance sensor -> edge AI computer (sensor fusion, detection, priority scoring) -> ROS 2 mission planning -> PX4 flight controller -> motors. A safety layer (override, geofence, failsafe) and a ground station support the flight.

## Proposed hardware (see docs/BOM.csv)
Holybro X500 V2 frame kit, Pixhawk 6C (PX4), NVIDIA Jetson Orin Nano, FLIR Lepton 3.5 thermal camera, IMX477 RGB camera, TFmini-S LiDAR, M9N GPS, 4S LiPo battery.

## Project status
| Stage | Status |
|---|---|
| 1. Concept, architecture, BOM, wiring plan | Complete |
| 2. Simulation (PX4 SITL, Gazebo, ROS 2, detection model) | In progress |
| 3. Hardware build and sensor integration | Planned |
| 4. Controlled validation and safety tests | Planned |

## Repository structure
- `docs/` project report, diagrams, BOM
- `cad/` mechanical design files
- `electronics/` wiring and schematic files
- `simulation/` PX4 / Gazebo setup
- `ros2_ws/src/` ROS 2 mission-planning packages
- `ai/` victim-detection model work

## Notes
Specifications and costs are design targets and estimates, to be validated through simulation and controlled testing. All flight testing will follow DGCA drone regulations.
