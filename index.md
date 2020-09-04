# Abstract 
Reward function specification can be difficult, even in simple environments. Rewarding the agent for making a widget may be easy, but penalizing the multitude of possible negative side effects is hard. [In toy environments](https://arxiv.org/abs/1902.09725),  Attainable Utility Preservation (AUP) avoided side effects by penalizing shifts in the ability to achieve randomly generated goals. We scale this approach to large, randomly generated environments based on Conway's Game of Life. By preserving optimal value for a single randomly generated reward function, AUP incurs modest overhead while leading the agent to complete the specified task and avoid side effects.

# SafeLife


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


## ```prune-still-easy```
<p align="center">
<img alt="prune-still-easy, PPO" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/prune-still-easy_ppo-min.gif"/>
<img alt="prune-still-easy, AUP" src="https://raw.githubusercontent.com/avoiding-side-effects/avoiding-side-effects.github.io/master/assets/gifs/prune-still-easy_aup-min.gif"/>
</p>
