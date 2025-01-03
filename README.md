🧭 Art_AI
🚀 Art_AI is a reinforcement learning project that brings life to a 2D minimap environment! Using Proximal Policy Optimization (PPO), the AI learns to explore, clear fog-of-war, and navigate a procedurally generated maze. Whether you're a reinforcement learning enthusiast or looking for a practical project to explore dynamic AI training, this repository has got you covered!

🌟 Features
Procedurally Generated Environment: A dynamic minimap with fog-of-war and maze chunks.
Reinforcement Learning: Powered by PPO for efficient policy optimization.
Checkpoints: Periodic model saves to prevent losing training progress.
Real-time Debugging: Colorful logs to track actions, rewards, and environment updates.
Metrics Overview: Insightful training stats for detailed performance monitoring.
🛠️ How It Works
🌍 Environment:

A 2D minimap with fog-of-war mechanics, revealing the map as the AI explores.
The player starts at a central position and navigates using basic actions: up, down, left, and right.
🧠 Observation:

A flattened fog state representing the current visibility of the map.
The player's normalized position in the environment.
🎯 Reward System:

Positive rewards: For clearing fog and revealing new areas.
Negative rewards: For redundant or ineffective movements.
⚙️ Training Algorithm:

PPO balances exploration and exploitation to optimize AI performance.
💾 Checkpoints:

Models are periodically saved in the /checkpoints directory.
Continue training from the latest checkpoint seamlessly.

📊 Metrics Explained

![image](https://github.com/user-attachments/assets/997545f7-a987-46b4-a670-fec58a9e5208)


🚀 Getting Started
1. Install Dependencies
Ensure you have Python 3.10+ and install the required libraries:

pip install stable-baselines3 gymnasium colorama numpy

2. Train the AI
Start the training process:

python train_ai.py

4. Monitor Training
Logs display actions, rewards, and fog-clearing updates in real time.
Checkpoints are saved in the /checkpoints directory.

6. Resume Training
To continue from the last checkpoint:

Place the checkpoint model in the project directory.
Modify train_ai.py to load the model:

model = PPO.load("checkpoints/model_checkpoint_x.zip", env=env)

5. Analyze Results
Metrics in the console give insights into the AI’s performance and convergence.
Use saved models for further testing or evaluation.

🤝 Contributions
Feel free to fork, contribute, or suggest enhancements!

💡 Inspiration
This project is inspired by video game mechanics and serves as a learning tool for reinforcement learning enthusiasts.

Happy exploring! 🎮

Repository Structure:

├── checkpoints/       # Saved models during training
├── minimap_env.py     # Environment logic and reinforcement learning setup
├── train_ai.py        # Training script with debugging and checkpoints
├── minimap_simulator/ # Visualization tools for the minimap
└── README.md          # Project description and instructions
