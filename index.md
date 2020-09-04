Reward function specification can be difficult, even in simple environments. Rewarding the agent for making a widget may be easy, but penalizing the multitude of possible negative side effects is hard. [In toy environments](https://arxiv.org/abs/1902.09725),  Attainable Utility Preservation (AUP) avoided side effects by penalizing shifts in the ability to achieve randomly generated goals. We scale this approach to large, randomly generated environments based on Conway's Game of Life. By preserving optimal value for a single randomly generated reward function, AUP incurs modest overhead while leading the agent to complete the specified task and avoid side effects.

# Experiments

In Conway's Game of Life, cells are alive or dead. Depending on how many live neighbors surround a cell, the cell comes to life, dies, or retains its state. Even simple initial conditions can evolve into complex and chaotic patterns. SafeLife turns the Game of Life into an actual game. An autonomous agent moves freely through the world, which is a large finite grid. In the eight cells surrounding the agent, no cells spawn or die – the agent can disturb dynamic patterns  by merely approaching them. There are many colors and kinds of cells, many of which have unique effects.

<p align="center">
<img alt="append-spawn, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-spawn_ppo-min.gif"/>
<img alt="prune-still-easy, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/prune-still_ppo-min.gif"/>
</p>

![](https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/img/explanation-caption.png)



## ```prune-still-easy```

<p align="center">
<img alt="prune-still-easy, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/prune-still_ppo-min.gif"/>
<img alt="prune-still-easy, AUP" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/prune-still_aup-min.gif"/>
</p>

## ```append-still-easy```
<p align="center">
<img alt="append-still-easy, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-still-easy_ppo-min.gif"/>
<img alt="append-still-easy, AUP" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-still-easy_aup-min.gif"/>
</p>


## ```append-still```
<p align="center">
<img alt="append-still, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-still_ppo-min.gif"/>
<img alt="append-still, AUP" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-still_aup-min.gif"/>
</p>


## ```append-spawn```
<p align="center">
<img alt="append-spawn, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-spawn_ppo-min.gif"/>
<img alt="append-spawn, AUP" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/append-spawn_aup-min.gif"/>
</p>

