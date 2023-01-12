# AutoSys-TurtlebotRos2
## Project to learn ROS2 by teaching a Turtlebot3 to follow a human using its camera

- At first the Turtlebot's Raspberry Pi takes a Picture with its Pycam and publishes it to a topic. This is done by our Picture Publisher Node.

- The Remote PC subscribes to this topic and calculates angular and linear velocity for the Turtlebot the picture with the Picture Processor Node. In Exchange, this Node then publishes the calculated velocities to cmd_vel.

- cmd_vel is subscribed by a built in Node from Turtlebot. It is launched by running the Turtlebot3 bringup Command, mentioned above. Now the Turtlebot drives accordingly.