# Exercise 3 - Self-Driving Trailer Agent Design

## 1. PEAS Framework
The PEAS framework describes the Performance measure, Environment, Actuators and Sensors of the self-driving trailer travelling from Nairobi to Kisumu.

* **Performance Measure:** Find the shortest route from Nairobi to Kisumu, successfully pass the goal test upon arrival, reach the destination safely, follow traffic rules, save fuel and deliver the cargo on time without damage.
* **Environment:** Kenyan highways, towns such as Nairobi, Nakuru, Kericho and Kisumu, other vehicles, pedestrians, traffic, potholes, roadblocks and weather conditions. 
* **Actuators:** Steering wheel for changing direction (including making left or right turns at town junctions), accelerator for increasing speed, brakes for slowing down or stopping, and indicators, lights and the horn. 
* **Sensors:** GPS and maps for identifying the trailer's current state or location, running goal tests and finding routes; cameras, radar and LiDAR for detecting obstacles; and a speedometer and odometer for tracking speed and distance. 

## 2. Five Definitions of the Agent's Environment

1. **Partially Observable or Fully Observable**
   * **On the actual road:** The environment is partially observable because the trailer cannot see everything around it. For example, fog, sharp corners and other vehicles may block its view.
   * **On the map:** The environment is fully observable because the agent has the map and the distances between towns before choosing a route.

2. **Stochastic or Deterministic**
   * **On the actual road:** The environment is stochastic because unexpected events can happen, such as traffic jams, sudden braking, rain or tyre problems.
   * **On the map:** The environment is deterministic because each route has a known destination and distance. For example, travelling from Nairobi to Nakuru takes the trailer to Nakuru at a fixed distance in the search model.

3. **Sequential**
   * The environment is sequential because each action affects what happens next. For example, choosing to travel through Nyeri instead of Nakuru changes the route and the total distance to Kisumu.

4. **Dynamic or Static**
   * **On the actual road:** The environment is dynamic because traffic, pedestrians and traffic lights can change while the trailer is moving.
   * **On the map:** The environment is static because the map stays the same while the agent searches for the shortest route.

5. **Continuous or Discrete, Single-Agent or Multi-Agent**
   * **Continuous vs. Discrete:** Actual driving is continuous because speed, steering and distance change over time. Map-based route planning is discrete because it uses specific towns as states and roads as connections between them.
   * **Single-Agent vs. Multi-Agent:** Actual driving is multi-agent because the trailer shares the road with other drivers and pedestrians, who have their own actions and goals. Map-based route planning is single-agent because the trailer searches for the best route on its own.
