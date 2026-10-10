# Autonomous Line-Following Minidrone: MathWorks Parrot Minidrone Competition India 2024

**Team Genzenith** · Vision-based flight control for the Parrot Mambo, designed in MATLAB/Simulink.

![MATLAB](https://img.shields.io/badge/MATLAB-R2023a-0076A8?logo=mathworks&logoColor=white)
![Simulink](https://img.shields.io/badge/Simulink-Parrot_Minidrone_Support_Package-orange)
![Result](https://img.shields.io/badge/result-Top_10_of_200_submissions-gold)
![License](https://img.shields.io/badge/license-GPL--3.0-green)

> 🏆 **Top 10** of 200 submitted designs, from more than 1,500 registrations.

---

## Mission

Using only the downward-facing camera, the drone must:

1. **Take off** and stabilise.
2. **Follow** a red line track of unknown shape, including sharp and acute turns.
3. **Detect** the circular marker at the end of the track.
4. **Land** precisely on it.

<p align="center">
  <img src="Tracks/Screenshot%202024-08-10%20093932.png" alt="Example competition tracks" width="640">
</p>

## Highlights

- **Fully autonomous** take-off → line following → marker detection → landing
- **Fast on sharp turns.** The controller handles acute angles that slow down typical line followers.
- **Stable tracking** through short, complex segments
- **Marker detection** for the landing circle

**Known limitation.** Very short segments between consecutive sharp turns can cause overshoot. These are rare on practical tracks.

## Repository Structure

```
.
├── MinidroneCompetition.prj        ← open this in MATLAB
├── controller/
│   └── flightControlSystem.slx     ★ Our flight control + image-processing algorithm
├── mainModels/
│   └── parrotMinidroneCompetition.slx   Top-level simulation model, plus parameters and sensor calibration
├── Tracks/                         35 test tracks (CSV waypoints) + reference images
├── nonlinearAirframe/              Nonlinear 6-DOF airframe model
├── linearAirframe/                 Trimmed / linearised airframe
├── libraries/                      Dynamics and environment block libraries
├── tasks/, utilities/, support/    Project setup scripts and helpers
├── tests/                          Model tests
├── resources/project/              MATLAB project metadata (do not edit by hand)
└── mathworks-minidrone-competition-guidelines.pdf
```

## Getting Started

### Requirements
- **MATLAB R2023a**. The project targets this release. Install the additional toolboxes the installer offers.
- **Simulink Support Package for Parrot Minidrones** (Add-On Explorer)

### Run the simulation
1. Clone the repository:
   ```sh
   git clone https://github.com/M-DOUSIK/Parrot-Minidrone-Competition-India-2024.git
   ```
2. Open **`MinidroneCompetition.prj`** in MATLAB. This sets up the paths and opens the 3D simulation model.
3. Choose a track: use the **Track Builder** or load one of the CSVs in `Tracks/`.
4. Run the simulation and watch the drone in the 3D visualiser.
5. To study or change the algorithm, open **`controller/flightControlSystem.slx`**.

## Competition Guidelines

The official rules and the scoring are in [`mathworks-minidrone-competition-guidelines.pdf`](mathworks-minidrone-competition-guidelines.pdf).

## Contributing

This repository is an archived competition entry and does not accept pull requests. Suggestions and ideas are welcome through Issues.

## License

[GPL-3.0](LICENSE). The base simulation framework is provided by MathWorks under its own terms.

## Contact

**Dousik Manokaran**: [m.dousik@gmail.com](mailto:m.dousik@gmail.com) · [LinkedIn](https://www.linkedin.com/in/dousikmanokaran/)
