---
layout              : page
show_meta           : false
title               : "Research Proposal"
subheadline         : "COMS BC3997 Project"
teaser              : "Feasible-Infeasible Two-Population (FI-2Pop) Genetic Algorithm Optimization for Voxel-based Soft Robots in Evolution Gym."
header:
   image_fullwidth  : "header_homepage_13.jpg"
permalink           : "/getting-started/"
---
1. Weeks 1-2: Exploration: Research overarching concepts, Generate a simple fi-2pop algorithm, Get acquainted with neural networks, evolutionary algorithms, and Evolution Gym.
1. Week 3-5: Execution: Write the actual Fi2-pop algorithm mwit ha fitness function suited for Voxel2 based robots.
1. Weeks 4-5: Testing: Simulate in Evolution Gym.
1. Weeks 6-8: Revisions: Make changes to algorithms to optimize execution in Evolution Gym.
1. Weeks 6-8: Analysis: Run statistical analysis on performance of algorithms in COMPARISON with others in Evolution Gym.
1. Iterate.
1. Weeks 9-10: Week Learn ins and outs of academic writing: read more articles, write an annotated bibliography, practice writing.
1. Weeks 10-15 (throughout research process): Paper: Generate a written research paper on the subject, collaborate with Lily Seoror on physical robots to generate cumulative research paper.

Topic/Overview (Objectives, outcomes):

Evolutionary algorithms allow inspection of all aspects of robotics simultaneously: morphology, motor systems, controller, and body. EAs lie at the intersection of biology, mathematics, and physics. The authors examine who is impacted by ERs, applications of the scientific method, and their issues and expected results. 

M.I.T researchers have developed Evolution Gym that seeks to use evolutionary algorithms with soft robots. Engineers and designers tend to model bodies of robots after pre-existing entities that already complete the job; however, this technology seeks to evolve robots to specific jobs to optimize functionality not encompassed by physical models. 
The Evolution Gym relies on two algorithms: an algorithm that generates the preliminary robot designs (design-optimization algorithm), and an algorithm that measures and scores their performance (control-optimization algorithm). By determining the fitness, they allow the soft robots to perform simple tasks such as traversing a minimal terrain, moving a box, climbing, etc. Essentially, what is already observed is the robots select for traits that do not necessarily replicate human or pre-existing being functioning. It is open-sourced, and can be used in our research by:
1. Use as benchmark to create and test our own algorithms
2. Measure how differently algorithms stack up
With Evolution Gym, it creates a smaller environment specifically for voxel-based soft-robots, a field of robotics that is not greatly explored. This research project seeks utilize all aspects of Evolution Gym to examine the genetic Feasible-Infeasible Two-Population algorithm for making comparisons between algorithms to optimize soft robot co-design by answering the following questions:
1. Successfully create a fi2pop algorithm for robots, specifically
2. Is the Fi2Pop algorithm more ideal for robotic evolution compared with other algorithms?
3. Is FI-2pop a better algorithm to induce diversity among robot populations?
4. How are different algorithms optimized for Evolution Gym?
5. How can we adjust the algorithms or analyze them to most reduce the reality gap?

Professor Soros’ mission: 
Professor Soros’ ultimate goal is to explore the applications of evolutionary algorithms on open-ended search specifically with focuses in robotics and content generation in video games. Specifically, she is interested in evolutionary and biological processes in computing and artificial life. By using pre-existing phenomena that dictate the living world, scientists are able to create more robust robots. This research project will allow exploration into applying a typical procedural content generation algorithm to soft robots, something that has not yet been explored. 

Problem statement (what is missing?):

Many studies in Evolutionary Robotics study how we can evolve robots generally using a standard EA algoirhtm. Few use feasible-infeasible methodoloogies of categorically dumping robots in buckets of “fit” and “unfit”. That being said, this process seeks to analyze the otpimziation and ability of the FI2Pop algorithm.
There is a distinct intersection between simulation and physical realization of robot evolution. Practically, Eiben deeply outlines the “Stages of Life '' of robotic evolution and specifics ways to combat obstacles of time, space, and resources - all having applications to simulations as well. Many explorations are founded in how we can evolve robots, generally not which algorithm is optimal for robot evolution. My part of the project is on the simulator end. How can we apply these genetic algorithms for voxel 2 based robots specifically? Additionally, research tends to focus on solely simulation or solely software, both having their own drawbacks. Although this individual project in scope is only in simulation, it has a role with tangible robots in Soros’ lab, decreasing the “reality gap”. This specific research relies on optimism that the evolution of robots lies in the foreseeable future, enabled by the hybridization with simulation to optimize efficiency of the complex evolutionary process.
Overall, This project seeks to explore the concept of failure in evolution and devise evolutionary algorithms that search through spaces of things that would normally be discarded by traditional EAs.


Method (What does it entail?/ What will it take for me to learn?):
With little knowledge of applications of evolutionary algorithms to robotics rather than procedural content generation in games, I must start from square one of “what is an evolutionary algorithm?” to  “how can Evolution Gym be used to simulate the algorithms?”. The project is multi-fold with aspects in understanding and writing academically as well as coding in general. It is a “sneak peak” into academic research projects. That being said, I have split the project into exploration, process, and analysis: 

Exploration:
1. Learn python, basics of evolutionary algorithms
2. Learn Git and collaboration in Git
3. Do readings: Create a annotated bibliography of all the research topics
4. Preliminary literature review (analyze specific algorithms that already exist)

Process:
1. Write own FI2Pop algorithm
2. Run algorithm with many iterations in Evolution Gym
3. Run other algorithm for documentation

Analysis:
1. Compare algorithms in Evolution Gym
2. Analyze performance of own algorithm
3. Learn ins and outs of academic writing
4. Read papers of feasibility of robot generation in simulated environments
5. Learn how to read papers effectively 

Conclusion (all in all, why is it important?):
Robot design and generation traverse a space that is confined to what the researchers think. The scope of design rarely ever diverges from pre-existing entities. Evolutionary algorithms allow computers and robots to do their own job of generation and manufacturing. They help taxing problems, which have applications in robotics, gaming, biology, and even sociology. The development of these algorithms allows for researchers to streamline their production process to optimize for a certain quantity such as materials, speed, a certain motion, etc. Given that the FI2Pop algorithm, in particular, has not been developed yet, we are able to compare it with other algorithms in a pre-existing space, Evolution Gym.




<a class="radius button small" href="{{ site.url }}{{ site.baseurl }}/documentation/">Check out the documentation for all the tricks ›</a>


 [1]: {{ site.url }}{{ site.baseurl }}/documentation/
