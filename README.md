# Java-LeJOS-Maze-Solver

This project focused on implementing the Pledge Algorithm in Java using leJOS on the LEGO Mindstorms EV3 platform. The objective was to design a robust maze-solving behavior capable of escaping complex looped mazes while maintaining accurate heading control and stable navigation.

The software architecture was built around a structured state-based control loop. A gyroscope continuously tracked heading, allowing the robot to maintain a fixed global direction reference — a core requirement of the Pledge Algorithm. When encountering an obstacle detected by ultrasonic sensors, the robot entered a wall-following state while tracking cumulative turn angle. Once the net rotational offset returned to zero and the original heading was clear, the robot exited wall-following and resumed forward traversal.

A key focus was maintaining straight-line stability. We implemented proportional heading correction using gyro feedback to reduce drift during forward motion. Sensor fusion between ultrasonic distance readings and gyroscopic angle data ensured smooth transitions between navigation states.
