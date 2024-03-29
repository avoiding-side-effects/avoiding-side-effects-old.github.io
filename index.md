Reward function specification can be difficult, even in simple environments. Rewarding the agent for making a widget may be easy, but penalizing the multitude of possible negative side effects is hard. [In toy environments](https://arxiv.org/abs/1902.09725),  Attainable Utility Preservation (AUP) avoided side effects by penalizing shifts in the ability to achieve randomly generated goals. We scale this approach to large, randomly generated environments based on Conway's Game of Life. By preserving optimal value for a single randomly generated reward function, AUP incurs modest overhead while leading the agent to complete the specified task and avoid side effects.

# Experiments

In Conway's Game of Life, cells are alive or dead. Depending on how many live neighbors surround a cell, the cell comes to life, dies, or retains its state. Even simple initial conditions can evolve into complex and chaotic patterns. 

[SafeLife](https://www.partnershiponai.org/safelife/) turns the Game of Life into an actual game. An autonomous agent moves freely through the world, which is a large finite grid. In the eight cells surrounding the agent, no cells spawn or die – the agent can disturb dynamic patterns  by merely approaching them. There are many colors and kinds of cells, many of which have unique effects.

<p align="center">
<img alt="append-spawn, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-spawn_ppo-min.gif"/>
<img alt="prune-still-easy, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/prune-still_ppo-min.gif"/>
</p>

![](https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/img/explanation-caption.png)

As the environment only rewards pruning red cells or creating gray cells in blue tiles, unpenalized RL agents often make a mess of the green cells (as shown above). The agent should "leave a small footprint" by not disturbing unrelated parts of the state, such as the green cells. Roughly, SafeLife measures side effects as the degree to which the agent disturbs green cells.

For each of the four following tasks, we randomly generate five curricula of 8 levels each. For each curriculum, we randomly sample a test-time trajectory from the baseline and AUP policy networks. The side-by-side results are shown below; for quantitative results, see our paper.

## prune-still-easy

The agent is rewarded for destroying red cells. After enough cells are destroyed, the agent may exit the level.

<p align="center">
<img alt="prune-still-easy, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/prune-still_ppo-min.gif"/>
<img alt="prune-still-easy, AUP" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/prune-still_aup-min.gif"/>
</p>

## append-still-easy

The agent is rewarded for creating gray cells on light blue tiles. After enough gray cells are present on blue tiles, the agent may exit the level.

<p align="center">
<img alt="append-still-easy, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-still-easy_ppo-min.gif"/>
<img alt="append-still-easy, AUP" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-still-easy_aup-min.gif"/>
</p>


## append-still

```append-still-easy```, but with more green cells.

<p align="center">
<img alt="append-still, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-still_ppo-min.gif"/>
<img alt="append-still, AUP" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-still_aup-min.gif"/>
</p>


## append-spawn

```append-still```, but with noise generated by stochastic yellow spawners.

<p align="center">
<img alt="append-spawn, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-spawn_ppo-min.gif"/>
<img alt="append-spawn, AUP" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-spawn_aup-min.gif"/>
</p>

