# DeepLearningCars 🏎️
An autonomous driving simulation built with **Pygame**, evolving from genetic algorithms (NEAT) to Reinforcement Learning (**DQN**).

## 🚀 Overview
This project simulates a car learning to navigate a track using sensor-based inputs (raycasting). The goal is to optimize the car's driving behavior so it can complete laps without hitting boundaries.

## 🛠️ Tech Stack
* **Language:** Python 3.9
* **Physics/GUI:** Pygame
* **Deep Learning:** PyTorch (DQN)
* **Data Handling:** NumPy (< 2.0)

## 📡 Sensors & Inputs
The car uses 7 "radar" sensors (raycasting) at specific angles:
`[-90, -60, -30, 0, 30, 60, 90]`
These sensors return normalized distances to the nearest track boundary, which are fed into the neural network to determine the best steering and throttle actions.

## 🧠 The Brain (DQN)
The project currently implements a **Deep Q-Network**:
* **Input Layer:** 7 sensor readings + current velocity.
* **Output Layer:** Discrete actions (Turn Left, Turn Right, Accelerate, Brake, Do Nothing).
* **Experience Replay:** Stores past experiences to break correlation in training data.

## ⚙️ Installation & Setup
1. **Clone the repo:**
   ```bash
   git clone [https://github.com/AlecDerinBorque/DeepLearningCars.git](https://github.com/AlecDerinBorque/DeepLearningCars.git)
   cd DeepLearningCars
