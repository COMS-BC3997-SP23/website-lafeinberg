---
layout: page-fullwidth
title: "Weekly updates"
subheadline: "Week 1"
meta_teaser: "Week #1 and Week #2 focused primarily on understanding what Evolutionary Algorithms are. I completeing reading assisgnments on what researchs NEEDS to be done in EAs to craft a proposal that made sense for 1. Professor Soros' research, 2. What needs to be done in the field, and 3. What is interesting and feasible for me."
teaser: "Week #1 and Week #2 focused primarily on understanding what Evolutionary Algorithms are. I completeing reading assisgnments on what researchs NEEDS to be done in EAs to craft a proposal that made sense for 1. Professor Soros' research, 2. What needs to be done in the field, and 3. What is interesting and feasible for me."
header:
    #image: evogym-1.jpg
    background-color: "#262930"
    caption: This is a caption for the header image with link
    caption_url: https://unsplash.com/
# image:
#     thumb:  homepage_typography-thumb.jpg
#     homepage: homepage_typography.jpg
#     caption: Image by Antonio
#     caption_url: "http://www.aisleone.net/"
categories:
    - design
    - typography
---
<!--more-->


## Checklist

+ Read papers
+ Background papers
+ Read papers
+ Set up evolution gym (include link to video)
+ Problem: incompatible with Evolution Gym

<!-- <div class="row">
<div class="medium-4 medium-push-8 columns" markdown="1">
<div class="panel radius" markdown="1">
**Table of Contents**
{: #toc }
*  TOC
{:toc}
</div>
</div><!-- /.medium-4.columns -->
<!-- 
<div class="medium-8 medium-pull-4 columns" markdown="1"> --> -->

## Reading #1: The Nature of Code, By Daniel Shiffman

Evolutionary algorithms are a class of optimization algorithms inspired by the process of natural selection in biological evolution. They are used to find solutions to complex problems by mimicking the process of natural selection, where the best-fit individuals survive and reproduce, passing on their genetic traits to the next generation.

Evolutionary algorithms work by iteratively generating a population of candidate solutions to a problem, evaluating their fitness or performance, and then selecting the fittest individuals to "reproduce" and create a new generation of candidate solutions. This process of selection, crossover, and mutation is repeated over multiple generations until an optimal or satisfactory solution is found.

There are different types of evolutionary algorithms, including genetic algorithms, evolution strategies, and genetic programming, among others. These algorithms have been applied to a wide range of problems, including optimization, machine learning, robotics, and more.

(INSERT PICTURE)


## Reading #2 Real-World Robot Evolution: Why Would it (not) Work?, by A.E Eiben

A.E Eiben explores merits, drawbacks, and possibility of fabricating a physical robot evolution. The main relevance in the study are the stages of robot evolution and the intersection between simulation and physical realization of robot evolution. Practically, Eiben deeply outlines the “Stages of Life '' of robotic evolution and specifics ways to combat obstacles of time, space, and resources - all having applications to simulations as well. 

The ultimate process of robot creation has many decisions: what are the degrees humans should be involved in selection and reproduction (the four systems of robot evolution, pages 3-4)?, when/should robots go through an internal stage of “learning” during “infancy” (learning and robot infancy, pages 4-5)?, to what extent should digital evolution replicate a biological one (genotype filtering, pages 6-7)?, and how can we use simulation and physical fabrication hand in hand (hydrid evolution: two populations, one species, page 7)? All of these questions are answered through addressing the impending issues regarding the practicality of simulations, time/space, and complexity of evolution. Subsequently, the author outlines practical steps of robot evolution, indicating for it to work, researchers much automate the evaluation of robot behavior, use EAs to evolve robot learning during infancy, define a controller trait space that
Identify peropties that capture and quantify aspects of robotic brains. All said, Eiden is optimistic that the evolution of robots lies in the foreseeable future, but must rely on hybridization with simulation to optimize efficiency of the complex evolutionary process.

## Reading #3: Evolutionary robotics: what, why, and where to, by Doncieux et al.
Doncieux et al. outline the basis of Evolutionary Algorithms and how it allows inspection of all aspects of robotics simultaneously: morphology, motor systems, controller, and body. EAs lie at the intersection of biology, mathematics, and physics. The authors examine who is impacted by ERs, applications of the scientific method, and their issues and expected results. 
Biologists and engineers can optimize robotics to explore their individual facets: engineers can create a holistic approach to robot design, extend design space, and intertwine simulation with models. Conversely, biologists may be able to study the evolutionary process itself, as we only observe one evolutionary system (Earth). Subsequently, Doncieux et al. explore how people can contribute to the field, specifically outlining effect methods to generate questions (mentioned below). Given the stochastic nature of EAs, research must be done in trials. They then delve into specific subfields of ERs: neural networks for a good controller paradigm, performance oriented fitness, selective pressure, and complexification. Finally, they outline the problems with ERs, including projecting the robots in the real world, whether Earth evolution is the benchmark for all evolutionary processes, the intersection between evolution and learning. In addition, evolutionary robotics can also be used to answer non-techinical questions such as the relation between the mind and body, definition of intelligence, evolution on social behaviors, and existence. It is clear that there is still much to learn to improve robotics, optimize the algorithms, and project them into the world. The whole process has barriers and questions such as the existence of an operational period, the “reality gap”, and the roles of humans in the process. With all considered, it is optimal in generating systems that holistically considers the evolution of agents or a broader system. Thus, this process can be used to analyze large scale models of populations to model phenomena that are difficult to study whether it be evolution, robotic control systems, or the concept of intelligence itself.

Steps for creating a question:
+ Determine main context of question
+ Come up with answerable questions
+ Generate a hypothesis
+ The question must be answerable and concnievedble after many iterations + through the algorithm. (The process must rely on multiple trials).
+ What would the results imply? What kind of results would validate or refute the hypothesis?


## Reading #4: Evolution Gym Sculpts Novel Robot Bodies and Brains

M.I.T researchers have developed Evolution Gym that seeks to use evolutionary algorithms with soft robots. Engineers and designers tend to model bodies of robots after pre-existing entities that already complete the job; however, this technology seeks to evolve robots to specific jobs to optimize functionality not encompassed by physical models. 
The Evolution Gym relies on two algorithms: an algorithm that generates the preliminary robot designs (design-optimization algorithm), and an algorithm that measures and scores their performance (control-optimization algorithm). By determining the fitness, they allow the soft robots to perform simple tasks such as traversing a minimal terrain, moving a box, climbing, etc. Essentially, what is already observed is the robots select for traits that do not necessarily replicate human or pre-existing being functioning. It is open-sourced, and can be used in our research by:
Use as benchmark to create and test our own algorithms
Measure how differently algorithms stack up
With Evolution Gym, it creates a smaller environment specifically for voxel-based soft-robots, a field of robotics that is not greatly explored. 

## Reading #5: Evolution Gym: A Large-Scale Benchmark for Evolving Soft-Robots
Evolution Gym surrounds finding the ideal robot “design” rather than “control”. Evolution Gym is the first software to attempt to co-optimize both the design and the control. It creates an environment that contains tasks including locomotion and manipulation of different terrains. They combine RL with optimization techniques to simulate complex evolution within those envrionments.
The purpose of the Evolution Gym is to explore co-design to solve problems regarding 1. The long control optimization loop, 2. Provide a platform to test different algorithms. 




## Defining overall concepts:
Evolutionary Algorithms Merits and Drawbacks
:   Can be used as a foundation for evolutionary robots. Although they work under multiple otimza, noise, lack of analytical models, there is an inevitable time scale and limitations in complexity of co-evlvoning the brain and body of robots.

Evolutionary robotics
:   Field for using evolutionary algorithms for designing and optimizing the body and brain of “real” robots”. 

Robot evolution
:   The fabrication and system of tangible robots reproducing in our physical environment. 

Four System Types
:   A proposed taxonomy that partitions the degree of human intervention in selection and reproduction (Type 1: Full human intervention in breeding and selection, Type 4: robot autonomy in reproduction and selection).

Optimization vs. Adaption
:   The difference between type 1 and 4- robots in type 1 can optomize themselves for a specific constrint or optima (optimize), while type 4 is dynamic to the environment (adapts and optimizes).

Stages of Life
:   Morphogenesis: Creating robot phenotype based on genotype, Infancy: “learning”, Maturity: Unsupervised learning and operation phase.

Double evolutionary system
:   Pseudocode that outlines the evolutionary system of “infancy”, where an outer loop optimizes the brian and body, nesting the inner loop optimizes the controller in a fixed body.

Hybrid evolution
:   Co-use of simulation and physical robots to accelerate finding “optimimal” body for a robot in simulation while realizing it to improve accuracy using physical robots.