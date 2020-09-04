# Abstract 
Reward function specification can be difficult, even in simple environments. Rewarding the agent for making a widget may be easy, but penalizing the multitude of possible negative side effects is hard. [In toy environments](https://arxiv.org/abs/1902.09725),  Attainable Utility Preservation (AUP) avoided side effects by penalizing shifts in the ability to achieve randomly generated goals. We scale this approach to large, randomly generated environments based on Conway's Game of Life. By preserving optimal value for a single randomly generated reward function, AUP incurs modest overhead while leading the agent to complete the specified task and avoid side effects.

# Demonstrations
<p align="center">
<img alt="benchmark level append-still-013, no impact penalty" src="https://github.com/PartnershipOnAI/safelife-videos/blob/master/v1.0/benchmark-append-still-013_p=0.gif?raw=true"/>
<img alt="benchmark level prune-still-003, no impact penalty" src="https://github.com/PartnershipOnAI/safelife-videos/blob/master/v1.0/benchmark-prune-still-003_p=0.gif?raw=true"/>
</p>
