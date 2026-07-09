# Adaptive Traffic Signal Control for Pedestrian Safety

A reinforcement learning-based adaptive traffic signal control system developed to improve pedestrian safety and reduce traffic waiting times at signalized intersections.

The system uses the SUMO (Simulation of Urban MObility) traffic simulator and compares four reinforcement learning algorithms:

- Deep Q-Network (DQN)
- Advantage Actor-Critic (A2C)
- Proximal Policy Optimization (PPO)
- Quantile Regression Deep Q-Network (QR-DQN)

The project evaluates how different reinforcement learning agents can dynamically control traffic signal phases based on real-time pedestrian and vehicle conditions.

## Project Overview

Traditional fixed-time traffic signals may not respond effectively to changing traffic and pedestrian conditions. This project develops an intelligent traffic signal control system that dynamically selects appropriate traffic light phases according to the current simulation state.

The reinforcement learning environment considers information such as:

- Pedestrian waiting time
- Number of waiting pedestrians
- Vehicle waiting time
- Vehicle count for multiple lanes
- Current traffic signal phase
- Time spent in the current phase
- Pedestrian phase waiting time
- Traffic phase starvation

The goal is to improve traffic efficiency while giving appropriate consideration to pedestrian safety and waiting time.

## Key Features

- Custom reinforcement learning environment built with Gymnasium
- SUMO-based traffic and pedestrian simulation
- Real-time communication with SUMO using TraCI
- Dynamic traffic signal phase selection
- Safe predefined vehicle and pedestrian traffic phases
- Pedestrian waiting-time monitoring
- Vehicle queue and waiting-time monitoring
- Reinforcement learning model training and evaluation
- Comparison of DQN, A2C, PPO and QR-DQN
- Training reward and learning stability visualization
- Hyperparameter evaluation for QR-DQN
- GUI-based simulation testing

## Reinforcement Learning Algorithms

### Deep Q-Network (DQN)

DQN is a value-based reinforcement learning algorithm that uses a neural network to estimate action values and select traffic signal phases.

### Advantage Actor-Critic (A2C)

A2C combines actor and critic networks to learn both the policy and the value function.

### Proximal Policy Optimization (PPO)

PPO is a policy-based reinforcement learning algorithm designed to provide stable and efficient policy updates.

### Quantile Regression Deep Q-Network (QR-DQN)

QR-DQN is a distributional reinforcement learning algorithm that models the distribution of future returns rather than predicting only a single expected value.

In this project, QR-DQN demonstrated strong overall performance in balancing pedestrian waiting time, vehicle waiting time and traffic control success.

## Technologies Used

- Python
- Jupyter Notebook
- SUMO
- TraCI
- Gymnasium
- Stable-Baselines3
- SB3-Contrib
- NumPy
- Pandas
- Matplotlib
- TensorBoard

## Project Structure

```text
adaptive-traffic-signal-reinforcement-learning/
│
├── AdaptiveTrafficSignalControl.ipynb
│
├── sumo_files/
│   ├── cross.con.xml
│   ├── cross.edg.xml
│   ├── cross.net.xml
│   ├── cross.nod.xml
│   ├── cross.rou.xml
│   ├── cross.sumocfg
│   └── view.xml
│
├── training_logs/
│   ├── dqn_rewards.npy
│   ├── dqn_lengths.npy
│   ├── a2c_rewards.npy
│   ├── a2c_lengths.npy
│   ├── ppo_rewards.npy
│   ├── ppo_lengths.npy
│   ├── qrdqn_rewards.npy
│   └── qrdqn_lengths.npy
│
├── dqn_traffic_model.zip
├── a2c_traffic_model.zip
├── ppo_traffic_model.zip
├── qrdqn_traffic_model.zip
│
└── README.md
