---
layout: page-fullwidth
title: "Weekly updates"
subheadline: "Week 3"
meta_teaser: "Week #3 Focused on downloading Evolution Gym software and writing up the code for a basic evolutionary algorithm. (Not FI2POP)."
teaser: "Week #3 Focused on downloading Evolution Gym software and writing up the code for a basic evolutionary algorithm. (Not FI2POP)."
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
# categories:
#     - design
#     - typography
permalink: /changelog/
---
 

 
<div class="flex-video"><iframe width="1280" height="720" src="https://youtu.be/L--IxUH4fac" frameborder="0" allowfullscreen></iframe></div><!-- /.flex-video -->

<div class="flex-video"><iframe width="1280" height="720" src="https://youtu.be/VWivmi9j608" frameborder="0" allowfullscreen></iframe></div><!-- /.flex-video -->

## This week I focused on creating an EA from scratch! I coded it up in java:

#### DNA.java
~~~

import java.util.*;
/**
 * 
 * @author lfein
 *
 */

public class DNA {
	// Properties in array could change depending on what we're trying to simulate
	// For example: DNA in physics system may be PVectors
	char[] genes = new char[18];
	
	// Fitness = Total # of characters correct/ Total # of characters
	String target = "to be or not to be";
	float fitness;
	
	// Mutation rate set to 0.01
	float mutationRate = (float)0.1;
	
	/**
	 * Randomly create each character of the array (randomly generated DNA)
	 */
	DNA() {
		for(int i = 0; i < genes.length; i++) {
			
			String possible = " abcdefghijklmnopqrstuvwxyz ";
			Random r = new Random();
			char c = possible.charAt(r.nextInt(28));
			
			genes[i] = c;
		}
	}
	
	// Updates the fitness by calculating a score
	void fitness() {
		int score = 0;
		for(int i = 0; i < genes.length; i++) {
			if(genes[i] == target.charAt(i)){ // is the character correct?
				score++; //If so, increment the score
			}
		}
		
		// Fitness is the percentage correct
		fitness= (float)(score)/target.length();
	}
	
	
	// REPRODUCTION 
	
	DNA crossover(DNA partner) {
		DNA child = new DNA();
		
		Random r = new Random();
		int midpoint = (int)(r.nextInt(genes.length)); // Pick random midpoint
		
		// Before midpoint, copy the DNA from parent B,
		// After midpoint, copy from parent A.
		for(int i = 0; i < genes.length; i++) {
			if (i > midpoint) 
				child.genes[i] = genes[i];
			else
				child.genes[i] = partner.genes[i]; 
		}
		
		return child;
	}
	
	// Look through the array and pick a character randomly to change according to mutation rate.
	void mutate() {
		
		Random r = new Random();
		
		for(int i = 0; i < genes.length; i++) {
			if(r.nextFloat() < mutationRate) {
				// Set charcter at i to a new raandom character.
				String possible = " abcdefghijklmnopqrstuvwxyz ";
				char c = possible.charAt(r.nextInt(28)); 
				genes[i] = c;
			}
		}
	}
	
	void printPhrase() {
		System.out.print("Current DNA: '");
		for(int i = 0; i<genes.length; i++) {
			System.out.print(genes[i]);
		}
		System.out.print("'");
	}
	

}
~~~

#### Main.java

~~~
import java.util.ArrayList;
import java.util.Random;

/**
 * Managing populations of DNA
 * @author lfein
 * Limitations: 
 * 1. Organisms can mate with themselves (parentA and parentB could be the same) --> reproduction
 * 2. The wheel of fortune algorithm will have extraordinarily high preference for some elements --> selection
 * 
 * TODO Features to add:
 * Report information about the progress of the genetic algorithm itself
 * Show the phrase closest to the target of each generation, average fitness
 * Stop genetic algorithm when a child is perfect
 */

public class main {
	
	// Create population of size 100
	static DNA[] population = new DNA[100];
	
	//Create empty mating pool
	static ArrayList<DNA> matingPool = new ArrayList<DNA>();
	
	static int MATINGROUNDS = 100000;
	
	public static void main(String[] args) {
		setup();
		draw();
		initalizeMatingPool();
		
		printPopulation("INITAL POPULATION");
		
		for(int i = 0; i < MATINGROUNDS; i++) {
			mate();
		}
		
		printPopulation("POPULATION AFTER ROUNDS");
		
	}
	
	// Initalize population
	static void setup() {
		for(int i = 0; i < population.length;i++) {
			population[i] = new DNA();
		}
	}
	
	//Call fitness function for each member of the population
	static void draw() {
		for(int i = 0; i < population.length; i++) {
			population[i].fitness();
		}
	}
	
	/**
	 * CREATING THE MATING POOL
	 * 
	 * The mating pool is a data structure from which we will continuously pick two parents.
	 * We want to pick parents with probabilities calculated according to fitness.
	 * Members of highest fitness scores most likely to be picked, but lowest still have chance.
	 * Similar to "spinning a wheel of fortune" with highest fitness scores more likely to be chosen.
	 * 
	 * We are going to have five options (ABCDE). In an Array list. We will ADD each parent to the list
	 * N amount of times equal to its percentage score.
	 */
	// Initialize mating pool
	static void initalizeMatingPool() {
			for(int i = 0; i < population.length; i++) {
				int n = (int)(population[i].fitness * 100);
				for(int j = 0; j < n; j++) {
					matingPool.add(population[i]);
				}
			}
	}
	
	/**
	 * Time to make babies.
	 * Pick two parents, perform reproduction.
	 */
	static void mate() {
		for(int i = 0 ; i< population.length; i++) {
			Random r = new Random();
			int a = (int)(r.nextInt(matingPool.size()));
			int b = (int)(r.nextInt(matingPool.size()));

			// use indicies to retrieve actual DNA instance from mating pool.
			DNA parentA = matingPool.get(a);
			DNA parentB = matingPool.get(b);

			// Mate and mutate the offspring. 
			DNA child = parentA.crossover(parentB);
			child.mutate();

			// Set new population reproduced
			population[i] = child;
		}
	}
	
	static void printPopulation(String msg) {
		System.out.println("DNA in population: \n" + msg);
		
		for(int i = 0; i < population.length; i++) {
			if (i%5 == 0) {
				population[i].printPhrase();
				System.out.println("");
			}
			else {
				population[i].printPhrase();
			}
		}
	}

}
~~~