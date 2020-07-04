#Title: Representation Learning in the Hippocampal-Entorhinal Circuit
##Speaker: Kim Stachenfeld
Link to talk: https://baicsworkshop.github.io/program/baics_44.html
Other links: https://neurokim.com

------------------------------------------

- Tolman, Cognitive Maps, 1948 --> through experiments with rodents, shows that animals learn structure even when it is not immediately rewarded
- O'Keefe & Dostrovsky, Hippocampus as a spatial map, 1971 --> place cells in hippocampus fire when an animal is in a particular place in space
- Hafting, Fyhn, Molden, Moser, Moser, Spatial map in the entorhinal cortex, 2005 --> grid cells, in the nearby region called entorhinal cortex, arranged as a hexagonal lattice having larger number of fields with spatially receptive firing patterns

Place cells -- encode physical location, non-spatial cues like sounds, are altered by experience (learn to fire earlier are the animal is forced to move along a specific direction of the track), have global remapping (two places cells that fire together in one environment, might fire at different locations in another environment)

Grid cells -- spatially triggered, encode non-spatial cues, influenced by environemt, show NO global remapping -- captures structure of the environment that is invariant across episodes, rather than episode specific maps

Problems in RL: can be very sample inefficient coz
	-  RL agents only trying to maximize reward, leading them to discard info that is not related to the reward -- lot of info lost in environments with sparse rewards
	- state spaces can be high dimensional and can have slow coverage times

 What do we need in the representation for the agent, i.e problems that RL struggles with
 	1. What additional structure, besides reward, should we learn? -- predictive representation, i.e learn predictions about what comes next
 	2. How can we build the system such that the downstream RL process has fewer things to learn about? -- relates to compression, such that how do we learn the shortest description possible of the given problem

 Model for mapping: RL <--> Hippocampus
 	- Place cells = learn predictive representation, i.e specific predictions of what is going to happen next in the episode
 	- Grid cells = capture low-dim structure among predictions

 Place cells <--> Predictive representations == use successor reperesentation
 	- value = expected sum of rewards you will get over your future explorations = sum of total number of times you expect to visit each state in the environment * instantaneous reward on each visitation (== successor representation matrix, M * reward vector, R) --> since M caches long term effect of dynamics, the RL problem just needs to deal with learning the rewards
 	- advantages:
 		- faster learning
 		- transition info is preserved --> if goals change while environment dynamics are change the agent can quickly relearn
 		- learnable and scalable model
 		- model defined with respected to general variables, like state and temporal adjacency

Grid cells <--> compression of info == modeled as eigenvectors of successor representations
	- can capture coarser aspects of the transition structure in the environment
	- support (multiscale/hierarchical) learning and exploration
	- similar to PCA

Exploration
	- RL -- uses random sampling of actions that leads to a random walk -- can be very inefficient as the same space might be covered multiple times; also agent might get stuck in a portion of the environment
	- Animals -- use a a biased random walk / levy walk, such that it looks like they are randomly exploring, but at some point might take big steps that take them in completely new parts of the environment -- much better coverage statistics, as lesser re-covering of the same ground and lesser chance of getting stuck
	- to apply this 'biased walk' to the model, reweight the eigenvectors to change very slowly with respect to the representation -- allows to explore will respecting the structure of the environment
	Replay events -- when the animal is asleep you see the same activity replayed as if the animal were awake -- but they exhibit properties of random walk, instead of the exact experienced behavior
	- levy walk is good for exploration efficiency, but random walk during sleep is better for consolidation accuracy to learn the structural representations

------------------------------------------
------------------------------------------
#Title: Bridging Intelligent Robotics and Cognitive Science
##Speaker: Leslie Kaelbling
Link to talk: https://baicsworkshop.github.io/program/baics_45.html
Other links: https://www.csail.mit.edu/person/leslie-kaelbling
Focus: Making intelligent embodied systems

------------------------------------------
- Some properties of Intelligent behaviour:
	- flexible, robust, adaptable --> if the env is different from what we expect it to be, we can reason and figure out how to change in accordance; adapt to changes in physiology of the robot eg some part breaks down or in requirements of the owner in short or long time period
	- purposeful
	- long-horizon
- Ways to get insights into natural science for AI:
	a. understand brains at neuronal level and replicate in computers
	b. understand brains at functional/algorithmic level and replicate in computers
	c. understand animal behavior at input-output level and replicate behavior in computers
	d. replicate evolution in simulation to see where we end up --> limited by computational resources
	e. engineer intelligent systems and see if we end up with systems that resemble natural systems
- General representation and inference mechanisms to focus on for intelligent behavior (non-exhaustive, imperfect):
	- feedback control --> allows systems to be robust and adaptable
	- convolution in space and time --> operating on perceptual inputs in ways that gives more information about the external world
	- kinematics and motion planning
	- forward/backward causal planning --> I am currently in this situation, if I were to take these actions what would happen vs this is where I want to be how do I get there
	- abstraction over objects --> to be able generalize over objects and classes of objects
	- state abstraction/aggregation --> be able to move up and down abstractions about the state information
	- temporal abstraction --> if planning over a long horizon make coarse plans but with short horizons plan with finer granularity
	- utility maximization --> reason about agent's own utility as well as utility function of beings in the environment around the agent
 - Some important questions to be asked of natural intelligences for building intelligent robots:
 	- what kinds of knwowledge are innate in natural systems
 	- what kinds of approximations and suboptimalities can natural systems make while still be considered okay
 	- what kind of modularities exist in the brain that can be exploited by human engineers
 	- how do brains encode spatial information -- useful for short term obstacle avoidance, long-term navigation, manipulate limbs to grasp objects etc.
 	- what are the scales and mechanisms of learning in nature and how well do they extrapolate rather than interpolate (ANN are good at interpolation)
 	- what mechanisms keep animals from fruitlessly repeating unsuccessful actions
 	- how are models of other agents built by natural systems

------------------------------------------
------------------------------------------
#Title: Autism-inspired AI for Visuospatial and Social Reasoning
##Speaker: Maithilee Kunda
Link to talk: https://baicsworkshop.github.io/program/baics_46.html
Other links: https://my.vanderbilt.edu/mkunda/
Focus:

------------------------------------------

- 

------------------------------------------
------------------------------------------
#Title: Cognitive Technologies for making the invisible visible
##Speaker: Judy Fan
Link to talk: https://baicsworkshop.github.io/program/baics_47.html
Other links: https://psychology.ucsd.edu/people/profiles/jefan.html
Focus:

------------------------------------------
