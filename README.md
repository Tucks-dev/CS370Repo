# CS370Repo

# Project Reflection for my AI Maze Solver

## Brief Explanation of Work

For this project, I started with a provided deep Q-learning environment that included a simple maze (`TreasureMaze`), replay memory (`GameExperience`), and a training loop. The base code lacked some key features necessary.

We were given the following starter code:
- `TreasureMaze.py`: A class representing the maze environment.
- `GameExperience.py`: A class for storing episodes and managing experience replay.
- Several pre-written utility functions and configurations in the Jupyter notebook, such as:
  - `build_model()`: Builds the neural network model.
  - `show()`: Visualizes the maze and agent.
  - `play_game()` and `completion_check()`: Run simulations to evaluate model performance.

The core part of the project involved writing the logic in the `qtrain()` function. We were given pseudocode comments and tasked with implementing the Q-learning loop, including:
- Randomly selecting starting cells.
- Choosing actions using an epsilon-greedy strategy.
- Storing experiences and rewards.
- Training the neural network model using `model.fit()` based on the experience data.
- 
## Connecting Learning to Computer Science

### What Do Computer Scientists Do and Why Does It Matter?

Computer scientists turn messy, real-world problems into well-defined computations and then design algorithms that solve them reliably. That matters because the world rarely hands you “clean” problems—yet people still need robust, safe solutions. Here I treated “find the treasure efficiently” as a sequential decision problem and used reinforcement learning to learn a policy from experience. The bigger idea is that the same pattern shows up in robotics, recommendations, and scheduling systems.

> Human-level DRL models, such as those from DeepMind, have shown that neural networks can learn complex policies directly from high-dimensional input data (Mnih et al., 2015).

### How Do I Approach a Problem as a Computer Scientist?

I approach problems methodically:
1. **Define the objective** – maximize maze-solving efficiency.
2. **Map the pieces** – reward shaping, valid moves, agent memory.
3. **Design & implement** – a loop-based training system with performance metrics.
4. **Validate** – using win rate history and early stopping.
5. **Iterate** – fix bugs, adjust hyperparameters, and improve runtime performance.

This mirrors how teams at places like OpenAI and Google DeepMind ship learning systems: tight loops of implement, test, measure, refine.

### Ethical Responsibilities to End Users and Organizations

As a computer scientist, it's good practice to think ethically

- **Promote transparency**: Be clear about what the model can/can’t do and why it makes certain choices.
- **Prevent harm**: Prefer conservative defaults and guardrails, no “creative exploration” that could harm users in real apps.
- **Ensure inclusivity and fairness**: Design for a range of users and hardware; avoid hidden assumptions that lock people out.
- **Protect user data**: If user data is involved (e.g., in a real assistant), collect the minimum needed and protect it.

These themes follow responsible-AI guidance from Microsoft, Google, and OpenAI and scale from classroom projects to production systems.
