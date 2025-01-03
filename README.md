🧭 Art_AI<br /> 🚀 Art_AI is a reinforcement learning project that brings life to a 2D minimap environment! Using Proximal Policy Optimization (PPO), the AI learns to explore, clear fog-of-war, and navigate a procedurally generated maze. Whether you're a reinforcement learning enthusiast or looking for a practical project to explore dynamic AI training, this repository has got you covered!<br />

🌟 Features<br />
Procedurally Generated Environment: A dynamic minimap with fog-of-war and maze chunks.<br />
Reinforcement Learning: Powered by PPO for efficient policy optimization.<br />
Checkpoints: Periodic model saves to prevent losing training progress.<br />
Real-time Debugging: Colorful logs to track actions, rewards, and environment updates.<br />
Metrics Overview: Insightful training stats for detailed performance monitoring.<br />

🛠️ How It Works<br />
🌍 Environment:<br />
A 2D minimap with fog-of-war mechanics, revealing the map as the AI explores.<br />
The player starts at a central position and navigates using basic actions: up, down, left, and right.<br />

🧠 Observation:<br />
A flattened fog state representing the current visibility of the map.<br />
The player's normalized position in the environment.<br />

🎯 Reward System:<br />
Positive rewards: For clearing fog and revealing new areas.<br />
Negative rewards: For redundant or ineffective movements.<br />

⚙️ Training Algorithm:<br />
PPO balances exploration and exploitation to optimize AI performance.<br />

💾 Checkpoints:<br />
Models are periodically saved in the /checkpoints directory.<br />
Continue training from the latest checkpoint seamlessly.<br />

📊 Metrics Explained<br />
![image](https://github.com/user-attachments/assets/997545f7-a987-46b4-a670-fec58a9e5208)

<br />
🚀 Getting Started<br />
1. Install Dependencies<br />
Ensure you have Python 3.10+ and install the required libraries:<br />

pip install stable-baselines3 gymnasium colorama numpy<br />

2. Train the AI<br />
Start the training process:<br />

python train_ai.py<br />

4. Monitor Training<br />
Logs display actions, rewards, and fog-clearing updates in real time.<br />
Checkpoints are saved in the /checkpoints directory.<br />

6. Resume Training<br />
To continue from the last checkpoint:<br />

Place the checkpoint model in the project directory.<br />
Modify train_ai.py to load the model:<br />

model = PPO.load("checkpoints/model_checkpoint_x.zip", env=env)<br />

5. Analyze Results<br />
Metrics in the console give insights into the AI’s performance and convergence.<br />
Use saved models for further testing or evaluation.<br />
<br />
6. Concurrent Simulations<br />
To increase or decrease the number of concurrent simulations (parallel environments):<br />

Locate the following line in train_ai.py:<br />

env = make_vec_env(lambda: MinimapEnv(), n_envs=3)<br />
Adjust the n_envs parameter to set the number of parallel environments. For example:<br />
n_envs=1: Single environment simulation (slower training).<br />
n_envs=8: Eight parallel environments for faster training (requires more computational resources).<br />
Note: Higher n_envs values significantly speed up training but demand more CPU cores and memory. Adjust based on your hardware's capabilities.<br />

🤝 Contributions<br />
Feel free to fork, contribute, or suggest enhancements!<br />

💡 Inspiration<br />
This project is inspired by video game mechanics and serves as a learning tool for reinforcement learning enthusiasts.<br />

Happy exploring! 🎮

Repository Structure:<br />
<br />
├── checkpoints/       # Saved models during training
├── minimap_env.py     # Environment logic and reinforcement learning setup
├── train_ai.py        # Training script with debugging and checkpoints
├── minimap_simulator/ # Visualization tools for the minimap
└── README.md          # Project description and instructions
