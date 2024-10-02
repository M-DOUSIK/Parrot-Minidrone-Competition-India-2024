# Parrot Minidrone Competition - India 2024 By Team Genzenith

This project was developed for the **Parrot Minidrone Competition India 2024**, where it ranked in the **Top 10** out of 200 submissions and over 1500+ registrations. The primary objective of this project is to build an autonomous drone capable of stable takeoff, following a predefined line using a camera, and detecting and landing on a circular marker.

## Features
- **Autonomous Flight**: The drone can take off, follow a line, and land autonomously.
- **Fast and Efficient**: Capable of handling sharp, acute turns and completing tasks faster than typical competitors.
- **Stable Line Following**: Uses a camera to detect and follow a path, even during short, complex turns.
- **Marker Detection**: The drone can detect circular markers for landing.
- **Limitations**: It struggles only in scenarios with very short path turns, which are rare in practical conditions.

## Setup Instructions
To set up this project, follow the steps below:
1. Install **MATLAB R2023a**. Note that the project is only compatible with this specific version of MATLAB.
2. During the installation of MATLAB, ensure you install all extra packages prompted during the setup, even though some might be unnecessary to avoid any issues later.
3. Install the **Simulink Support Package for Parrot Minidrones**.

## Running the Project
1. Open the `.prj` file in MATLAB to access the 3D model of the drone and the algorithm simulation.
2. Go to the **Track Builder** tool to select or modify a path from the `tracks` folder.
3. Run the simulation and observe the drone's behavior in the virtual environment.
4. To explore or modify the algorithm, open the **Flight Control System**.

## Project Structure
- `.prj` file: Launches the simulation environment and the algorithm model.
- `tracks/`: Contains pre-built paths for the drone to follow.
- **Flight Control System**: The core algorithm controlling the drone's flight.

## Contribution Guidelines
Currently, this project does not accept contributions. However, new feature suggestions or enhancements from the community are welcome.

## Contact
For any queries or feedback, feel free to reach out via:
- Email: [m.dousik@gmail.com](mailto:m.dousik@gmail.com)
- LinkedIn: [Dousik Manokaran](https://www.linkedin.com/in/dousikmanokaran)

---

