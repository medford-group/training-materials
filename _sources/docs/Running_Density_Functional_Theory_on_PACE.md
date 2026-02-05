# Running Density Functional Theory on PACE

## Introduction

This section will introduce you to the basics of running density functional theory (DFT) calculations on PACE. We will use the Atomic Simulation Environment (ASE) and the sparc-dft-api to generate the input files for the DFT calculations, and we will use bash files to submit the calculations to PACE. We will also use ASE and sparc-dft-api to analyze the results of the calculations. We will introduce two DFT codes, Quantum Espresso (QE) and the Simulation Package for Ab-initio Real Space Calculations (SPARC). There are a number of differences between these two codes both conceptually (planewave vs real space) and technically (fortran vs C). However, both codes are open source and do not require a license to run. Both codes are also capable of running a number of different types of calculations, including geometry optimizations, molecular dynamics, and band structure calculations. All of these so called "electronic structure" methods are useful. However, we will focus on some of the more basic and common calculations, namely convergence tests, geometry optimizations, and adsorption energy calculations. We will introduce each of these in greater detail in later sections. Here, we are primarily concerned with getting the codes set up and running toy calculations on PACE. 

## Lectures

The lectures specifically cover using SPARC on PACE using the SPARC-X-API (https://sparc-x.github.io/SPARC-X-API/)
PACE.1 [Lecture 1](https://mediaspace.gatech.edu/media/RunningDFT_L01/1_rrdqc1z9)
PACE.2 [Lecture 2](https://mediaspace.gatech.edu/media/RunningDFT_L02/1_734pbtod)
PACE.3 [Lecture 3](https://mediaspace.gatech.edu/media/RunningDFT_L03/1_m0qaizlj)
PACE.4 [Lecture 4](https://mediaspace.gatech.edu/media/RunningDFT_L04/1_ycpigt8e)
PACE.5 [Lecture 5](https://mediaspace.gatech.edu/media/RunningDFT_L05/1_weur9bwl)
PACE.6 [Lecture 6](https://mediaspace.gatech.edu/media/RunningDFT_L06/1_9fsctzui)