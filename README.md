# Snake Game AI 🐍

This project is an implementation of the classic Snake game, with an AI agent that learns to play the game on its own. The AI is built using a Deep Q-Network (DQN) algorithm, which allows it to learn the optimal policy by interacting with the game environment.

<img width="791" height="682" alt="Screenshot 2025-08-20 154722" src="https://github.com/user-attachments/assets/5a59ae11-79dd-4b3c-9a50-a0546ad9a42a" />
<img width="633" height="503" alt="Screenshot 2025-08-20 154743" src="https://github.com/user-attachments/assets/a35d8f01-b841-4fc3-bea0-f95ae06699a8" />

---

## 🚀 Features

-   **Classic Snake Gameplay**: Enjoy the timeless game of Snake.
-   **AI Agent**: Watch an AI agent learn and master the game through reinforcement learning.
-   **Real-time Plotting**: Visualize the AI's training progress with real-time plots of scores and mean scores.
-   **Modular Code**: The code is organized into logical components for the game, agent, and model, making it easy to understand and modify.

---

## 🛠️ Technologies Used

-   **Python**: The core programming language.
-   **Pygame**: A set of Python modules designed for writing video games.
-   **PyTorch**: An open-source machine learning library used to build and train the neural network for the AI agent.
-   **NumPy**: A library for numerical operations, used for efficient data handling.
-   **Matplotlib**: A plotting library used to visualize the training progress.

---

## ⚙️ Setup and Installation

To get the project running on your local machine, please follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Sachin00028/SnakeGame-AI.git](https://github.com/Sachin00028/SnakeGame-AI.git)
    cd SnakeGame-AI
    ```

2.  **Create a virtual environment (recommended):**
    This will keep the project's dependencies isolated from your global Python installation.
    ```bash
    # For Windows
    python -m venv venv
    .\venv\Scripts\activate

    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install the required dependencies:**
    Use the `requirements.txt` file to install all necessary libraries.
    ```bash
    pip install -r requirements.txt
    ```

---

## ▶️ How to Run

Once you have completed the setup, you can run the game by executing the `agent.py` script:

```bash
python agent.py
```

This will start the game, and the AI agent will begin its training process. You will see the game window and a plot showing the agent's performance over time.

---

## 🧠 The AI Model

The AI agent uses a Deep Q-Network (DQN), a type of reinforcement learning algorithm. Here's a brief overview:

-   **State**: The state is a representation of the game environment provided to the agent. It includes information like the danger in front, left, or right of the snake, the direction of movement, and the location of the food.
-   **Action**: The agent can choose one of three actions at each step: go straight, turn left, or turn right.
-   **Reward**: The agent receives rewards based on its actions:
    -   **+10**: for eating the food.
    -   **-10**: when the game is over (colliding with a wall or itself).
    -   No reward otherwise.
-   **Learning**: The agent uses a neural network to approximate the Q-value for each possible action in a given state. It learns by minimizing the difference between its predicted Q-values and the "target" Q-values using the Bellman equation. This process is known as training.

The agent stores its experiences (state, action, reward, next state) in a memory buffer and samples from it to train the network, which helps in stabilizing the learning process.
