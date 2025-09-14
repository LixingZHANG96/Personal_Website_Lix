# Set Up the Follower Arm
## Overview
* **The [SO-101](https://huggingface.co/docs/lerobot/en/so101) Project**: LeRobot aims to provide models, datasets, and tools for real-world robotics in PyTorch. The goal is to lower the barrier for entry to robotics so that everyone can contribute and benefit from sharing datasets and pretrained models. The SO-101 and its pioneer project SO-100 are the names of the robot arms themselves.
* The SO-101 consists of 2 parts: A follower-arm and a leader-arm, they share almost the same structure, other than the shape of the 1-DoF-End-effector: 
  1. The follower has the shape of a crabapple, allowing it to pick up objects. On this concern, it renders a motor with lower gear ratio and higher input-voltage to reach a higher torsion. TODO: pic of follower.
  2. The leader consists of a grappler and a trigger, resembling the pistol grip. That proves to be an ergonomic friendly design for human hands. And of course, the torsion should be lower to ease up the operation. TODO: pic of leader
### Objectives
* Set up the mechanical structure of the SO-101 follower arm.
* Get the follower arm moving using keyboard or joystick.
## Details
### Hardware Setup
* The hardware parts, including servo motors, necessary cables and battery were purchased according to the [official BOM](https://github.com/TheRobotStudio/SO-ARM100?tab=readme-ov-file#sourcing-parts). Instead of STS3215 C001, which works under 7.4V, I have chosen STS3215 C018, which provides a higher torque under 12V.
* The parts are 3D-printed and assembled according to the [official guide](https://github.com/TheRobotStudio/SO-ARM100). TODO: Pic assembled
* The part WaveShare_Mounting_Plate did not suit good enough to the board itself. I have thus redesi	gned the part. TODO: pic waveshare_mount TODO: Link to the new part.
### Software Testing
* The initial installation was done on my desktop PC. Motor recognition, calibration was executed according to the [official guide](https://huggingface.co/docs/lerobot/en/so101). 
* A quick keyboard-control was conducted using the APIs provided by [Phosphobot](https://phospho.ai/). TODO: video keyboard control 1.
* After that, the process was repeated on a Raspberry Pi 5. 
# Result
The follower arm was successfully set up, ready for direct controlling and expansions.