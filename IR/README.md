GROUP 25

David Petrovic, david.petrovic@studenti.unipd.it

Federico Luisetto, federico.luisetto@studenti.unipd.it

Umberto Salviati, umberto.salviati@studenti.unipd.it
## Execution commands for 1st assignment
rosrun ass1_group25 server

rosrun ass1_group25 findCenter

rosrun ass1_group25 client X Y THETA

## Execution commands for 2nd assignment
roslaunch ass2_group25 start_assignment2.launch

rosrun ass2_group25 manager

# Intelligent Robotics Project - Group 25 A2

## Team Members
- David Petrovic (david.petrovic@studenti.unipd.it)
- Federico Luisetto (federico.luisetto@studenti.unipd.it)
- Umberto Salviati (umberto.salviati@studenti.unipd.it)

## Project Overview

### Abstract
The goal of our project is to implement a fetch and delivery behavior for everyday objects using a TIAGo robot by PAL Robotics. This involves scanning and identifying objects, understanding their positions, and executing pick-and-place operations. The implementation utilizes laser data for precise positioning during object placement.

## Project Repository
[Bitbucket Repository](https://bitbucket.org/fede-luis-ir/ir2324_group_25/src/master/)

## Documentation and Resources
[Project Google Drive](https://drive.google.com/drive/folders/1oHUEsZ28TrrXRZDUDC0CUJtkjIuJyRpl?usp=sharing)

## Table of Contents
1. [Introduction](#introduction)
2. [Group Information](#group-information)
3. [Human Node and Tiago Movement](#human-node-and-tiago-movement)
4. [Position of Colored Tables](#position-of-colored-tables)
5. [AprilTag](#apriltag)
6. [Pick and Place](#pick-and-place)
7. [Conclusions](#conclusions)

## 1. Introduction

In this project, we implemented a fetch and delivery behavior for a TIAGo robot. The robot scans, identifies, and places everyday objects on designated tables. Our solution is organized into a central node named "manager" that controls all execution, along with specialized nodes for object detection, pick-and-place tasks, colored table detection, and Tiago movement.

## 2. Group Information

Group 25 consists of David Petrovic, Federico Luisetto, and Umberto Salviati. For more details, refer to the [Bitbucket Repository](https://bitbucket.org/fede-luis-ir/ir2324_group_25/src/master/).

## 3. Human Node and Tiago Movement

The robot's movements are controlled by invoking the action server from assignment 1. The human node is called through the "human_srv" service, providing the sequence of object IDs for the pick-and-place phase.

## 4. Position of Colored Tables

Colored table positions are determined through a two-phase method. First, a detector node analyzes images from Tiago's camera, applying color filters to identify each table's position. In the second phase, laser scans from assignment 1 enhance precision by computing mean values from different perspectives.

## 5. AprilTag

After receiving object IDs from the human node and obtaining colored table positions, the robot moves to a fixed position near the table. The Tiago's camera focuses on objects using an action client connected to the control_msgs::PointHeadAction server. The detection service records object IDs and poses.

## 6. Pick and Place

The pick-and-place problem is implemented by the "arm_controller" node. The pick phase involves computing pre-grasp and post-grasp poses, while the place phase positions the arm above the target table. Collision objects are managed for safe and efficient object manipulation.

## 7. Conclusions

The team collaborated extensively, with each member contributing to different aspects of the project. Federico focused on the pick-and-place routine, David assembled and coded color and object detection, and Umberto assisted with table detection and debugging.

**Note:** For detailed technical information, please refer to the project documentation in the [Google Drive](https://drive.google.com/drive/folders/1oHUEsZ28TrrXRZDUDC0CUJtkjIuJyRpl?usp=sharing).
