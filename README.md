<a id="readme-top"></a>

<div align="center">
  
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

</div>

<br />
<div align="center">
  <h3 align="center">Autonomous Control and Navigation of a Lego Mindstorms Robot</h3>

  <p align="center">
    A MATLAB-based autonomous navigation system using global computer vision, Probabilistic Roadmap (PRM) planning, and semantic traffic sign recognition.
    <br />
    <br />
    <a href="https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation/issues">Report Bug</a>
    ·
    <a href="https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation/issues">Request Feature</a>
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## About The Project

This project focuses on the development of an autonomous control and navigation system applied to a Lego Mindstorms mobile robot, operating in a structured environment controlled exclusively by computer vision. The project aims to replace classic odometry and local sensorization with a global perception architecture. A camera in a top-down configuration provides the necessary data for metric mapping of the space and real-time localization of the vehicle.

The methodology integrates probabilistic trajectory planning algorithms (PRM) with point-to-point execution (Drive2Point) and continuous tracking (Pure Pursuit) kinematic controllers. Additionally, a semantic recognition module based on image processing was implemented, allowing the robot to identify traffic signs and make autonomous navigation decisions.

### Key Results & Performance
* **Global Vision Mapping:** Transformed 2D images into Binary Occupancy Grids by extracting metric information using a 150mm reference calibration.
* **Dynamic Localization:** Isolated objects of interest via HSV thresholding and morphological filters to extract centroids and accurately distinguish the robot's front and rear.
* **Autonomous Path Planning:** Successfully implemented PRM to generate collision-free routes, coupled with a Drive2Point controller that relies on a two-phase logic (turn-in-place followed by forward movement) to reach targets.
* **Traffic Sign Recognition:** Developed a module that detects blue signs, applies a circular mask to isolate the arrow, and calculates the centroid and tip to autonomously decide left or right turns.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

* [![MATLAB][MATLAB-shield]][MATLAB-url]
* [![Lego][Lego-shield]][Lego-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites

Ensure you have MATLAB installed on your machine with the following toolboxes:
* Image Processing Toolbox
* Navigation Toolbox

### Installation

1. Clone the repo:
   ```sh
   git clone https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation.git
2. Open MATLAB and navigate to the cloned repository folder.

3. Open the `Code.mlapp` file in MATLAB App Designer.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



## Usage

1. Run the `Code.mlapp` application to launch the Graphical User Interface (GUI).

2. Establish a connection with the top-down camera (via IP, USB, or local images).

3. Calibrate the HSV threshold parameters to accurately detect the robot and the obstacles/bases.

4. Set the waypoint order from the dropdown menus to define the robot's target sequence.

5. Select the preferred control method (Drive2Point or Pure Pursuit) and execute the path tracking.

_For a comprehensive demonstration, please refer to the [demonstration](Demo.mp4) video included in the repository, or read the detailed technical [report](Relatorio_TP2_Robotica.pdf)._
<p align="right">(<a href="#readme-top">back to top</a>)</p>



## Roadmap

- [x] Top-down metric mapping & Binary Occupancy Grid generation
- [x] Real-time spatial localization using HSV thresholding
- [x] Probabilistic Roadmap (PRM) integration
- [x] Drive2Point kinematic control implementation
- [x] Semantic traffic sign recognition (Left/Right decisions)
- [ ] Controller parameters calibration for floor friction and mechanical compensation
- [ ] Codebase and GUI optimization/refactoring
- [ ] Full transition to an onboard-camera navigation paradigm in a 3D environment

See the [open issues](https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Top contributors:

<a href="https://github.com/AlexBrindzz/aruco-project/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=AlexBrindzz/aruco-project" alt="contrib.rocks image" />
</a>

<p align="right">(<a href="#readme-top">back to top</a>)</p>



## License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



## Contact

Alexandre Sá Jesus - [LinkedIn](https://linkedin.com/in/alexandre-sa-jesus)

Project Link: [lego-mindstorms-autonomous-navigation](https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



## Acknowledgments

I would like to express my gratitude to the institutions and individuals who made this research project possible:

* [IPCA - Instituto Politécnico do Cávado e do Ave](https://ipca.pt/)
* **Ph.D. Pedro Morais** - For the guidance and technical supervision.
* **Co-authors** - [Luís Barrão](https://github.com/LewisLegstrong) and [Paulo Palhares](https://github.com/ParPalhares).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/AlexBrindzz/lego-mindstorms-autonomous-navigation.svg?style=for-the-badge
[contributors-url]: https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation/graphs/contributors

[forks-shield]: https://img.shields.io/github/forks/AlexBrindzz/lego-mindstorms-autonomous-navigation.svg?style=for-the-badge
[forks-url]: https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation/network/members

[stars-shield]: https://img.shields.io/github/stars/AlexBrindzz/lego-mindstorms-autonomous-navigation.svg?style=for-the-badge
[stars-url]: https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation/stargazers

[issues-shield]: https://img.shields.io/github/issues/AlexBrindzz/lego-mindstorms-autonomous-navigation.svg?style=for-the-badge
[issues-url]: https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation/issues

[license-shield]: https://img.shields.io/github/license/AlexBrindzz/lego-mindstorms-autonomous-navigation.svg?style=for-the-badge
[license-url]: https://github.com/AlexBrindzz/lego-mindstorms-autonomous-navigation/blob/main/LICENSE

[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/alexandre-sa-jesus

[MATLAB-shield]: https://img.shields.io/badge/MATLAB-e25f1c?style=for-the-badge&logo=mathworks&logoColor=white
[MATLAB-url]: https://www.mathworks.com/

[Lego-shield]: https://img.shields.io/badge/Lego_Mindstorms-D11013?style=for-the-badge&logo=lego&logoColor=white
[Lego-url]: https://www.lego.com/
