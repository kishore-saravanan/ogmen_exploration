# Ogmen Exploration

## Chosen Path Planning Algorithm:
The chosen path planning algorithm in this implementation is A* (A-star).
A* is a popular and widely-used search algorithm known for its optimality and efficiency in finding the shortest path in a weighted graph.
It is suitable for the task of robot path planning in a grid-based environment, as it can efficiently navigate through obstacles while minimizing the path length in an indoor environment.

## Implementation Details of the Path Planning Node:
The path planning node is implemented as a ROS node called astar_node.
It subscribes to topics for the occupancy map, start point, and target point, and publishes the inflated map and optimal path.
The node utilizes the A* algorithm implemented in the astar::Astar class for path planning.
Callback functions are implemented to handle map updates and receive start and target points.
Upon receiving all necessary inputs, the node triggers the path planning process, computes the optimal path, and publishes it for visualization.
occupancy_map_threshold and occupancy_map_inflation_radius are given as arguments and can be changed from the launch file.

## Instructions for Building and Running the ROS Package:
To build the ROS package containing the astar_node, follow these steps:

Create a ROS workspace if you haven't already.

Clone this package repo into the src directory of your workspace.

Install the required dependencies using rosdep.

Run catkin_make in the root of your workspace to build the package.

To run the ROS node:

Execute this command in a terminal:
> roslaunch ogmen_exploration exploration_turtlebot3.launch 


## Steps to Visualize the Computed Path in RViz:
In the Rviz window, you can see the map is being built as the robot moves to explore the environment.
