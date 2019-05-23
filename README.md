# DeepCars for OpenAI Gym

This is the registered version of DeepCars for the [OpenAI Gym](https://github.com/openai/gym) [environments](https://github.com/openai/gym/tree/master/gym/envs). DeepCars is a simple highway traffic simulator for training Reinforcement Learning agents to perform the high-level decision making on self-driving cars. The environment simulates the occupancy grid world around the ego vehicle.


```ruby
cd gym-deepcars  
pip install -r requirements.txt
pip install -e .
python DeepCars_test.py
```

Two versions are registered:
 
DeepCars-v0: observation space is occupancy grid (0: empty grid, 1: occupied with actor, 2: occupied with ego).
DeepCars-v1: observations space is a vector of distances to the closest actors in each lane + ego lane.

In both versions action space contains high-level actions: go to the left lane, stay in the current lane, and go to the right lane.

Reward function:

+1: at each step
-1: if collision occurs.
