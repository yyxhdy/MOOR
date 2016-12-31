# MOOR

This program mainly implements three multiobjective objective reduction algorithms. The key idea of these algorithms is to 
view objective reduction as a multiobjective search problem and then use a multiobjective evolutionary 
algorithm, i.e., NSGA-II, to derive a trade-off between the error and size of objective subset. 

Three algorithms are based on three different errors:

1) NSGA-II-Delta uses the delta error proposed in [1]. 

2) NSGA-II-Eta uses a new dominance structure-based error, referred to as eta. 

3) NSGA-II-Gamma uses a new error, referred to as gamma, which measures the change of correlation structure. 


****************************************************************************************************************************
The source code is written in Java and is modified based on jMetal. The source code of [1] provided by Brockhoff and Ziztler 
is also incoporated into our package.

The program uses an external archive, i.e., colt.jar, so make sure you have linked it to the build path before you run it. 

The multiobjective formations for NSGA-II-Delta, NSGA-II-Eta and NSGA-II-Gamma are implemented respectively
in OR_Delta.java, OR_Eta.java and OR_Gamma.java, respectively.


The package jmetal.objred.nsgaII contains two java files: NSGA-II.java implements the basic NSGA-II procedures, 
while NSGA-II-OR_main.java shows how to use NSGA-II solve the multiobjective 
formulations of the objective reduction problem, where the nondominated set is read from a plain text. 

The package jmetal.objred.brockhoff contains three java files: DeltaMOSSGreedyWrapper.java is the wrapper for 
the greedy algorithms in [1], while DeltaMOSSExactWrapper.java is the wrapper for the exact algroithm in [1]. 
DeltaMOSS_main.java shows how to usethe greedy or exact algroithm to solve a delta-MOSS or k-EMOSS probelm. 

****************************************************************************************************************************
Note that, this code can be used only for non-commercial purposes. 

For any problem concerning the code, please feel free to 
contact Dr. Yuan Yuan (yyxhdy@gmail.com).

****************************************************************************************************************************
Reference: 
[1] D. Brockhoff and E. Zitzler, ''Objective reduction in evolutionary multiobjective 
optimization: theory and applications,'' Evolutionary Computation, vol. 17, no. 2, pp. 135–166, 2009.
