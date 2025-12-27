# Traffic Lab Pro

Traffic Lab Pro is a real-time traffic intersection simulator built with HTML5 Canvas and vanilla JavaScript. It visualizes and measures the efficiency difference between static traffic light timers and dynamic, pressure-based AI control systems.

This project was built as a fun experiment to explore agent-based simulation, visualization techniques, and algorithmic efficiency.

## Features

* **Smart AI Control:** Implements a "Pressure System" algorithm that dynamically adjusts traffic light phases based on queue length and wait times.
* **Asymmetric Flow Control:** Allows users to independently adjust traffic density for horizontal and vertical roads to simulate realistic, unbalanced traffic scenarios.
* **Real-Time Analytics:** Displays live metrics for throughput (Cars Per Minute) and average wait times, visualized on a scrolling line graph.
* **Data Export:** Includes a CSV export feature to download simulation logs for external analysis.
* **Visual Engine:** Features a 2.5D isometric view with a dynamic day/night cycle, vehicle shadows, and reactive lighting.

## How to Run

1. Download the index.html file.
2. Open the file in any modern web browser (Chrome, Firefox, Edge, Safari).
3. No installation, build steps, or external dependencies are required.

## The Logic (The Pressure System)

The core "Smart AI" algorithm mimics real-world adaptive traffic signal control. It calculates a "pressure" score for each lane every frame using the following logic:

1. **Queue Pressure:** The number of cars waiting is raised to the power of 1.5. This non-linear scaling ensures that long queues are prioritized exponentially higher than short ones.
2. **Switching Logic:** The system only switches lights if the pressure on the red signal exceeds the pressure on the green signal by a specific threshold. This prevents rapid flickering and ensures smooth flow.
3. **Starvation Prevention:** If a lane has been waiting too long, the system forces a switch regardless of pressure to prevent vehicles from being trapped indefinitely.

## Controls

* **Flow Sliders:** Adjust the spawn rate of cars for Horizontal (West/East) and Vertical (North/South) roads independently.
* **Toggle Night Mode:** Switches the visual theme between day and night.
* **AI / Timer Button:** Toggles between the adaptive AI algorithm and a standard fixed-interval timer.
* **Download CSV:** Exports the current session's traffic data to a .csv file.

## Project Status

This is a personal hobby project created for educational purposes. It is open for modification and experimentation.

## License

MIT License. Free to use and modify.