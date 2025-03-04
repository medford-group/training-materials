# DFT adsorption energy reproducibility project

This project will explore a crucial, but often neglected, aspect of DFT research: reproducibility of results. There are a few papers on this topic (e.g.  [https://www.science.org/doi/10.1126/science.aad3000](https://www.science.org/doi/10.1126/science.aad3000)) but none that focus specifically on adsorption energies. Since adsorption energies are “derived quantities” – that is, they are not direct outputs of a single DFT calculation – they can be more challenging to reproduce. Our hypothesis is that by combining large-language models with natural language instructions, we can identify how to more robustly communicate instructions about how to reproduce DFT calculations, and provide specific insight into which “prompt engineering” strategies and LLM structures that are most effective for the task. Your project will help test this hypothesis by using LLMs to reproduce at least 3 adsorption energies found in the literature.

## Grading:

The details of the project are outlined below. The project should be **completed individually** although you are welcome to work with others or seek feedback from graduate mentors along the way. However, you should not reproduce any of the same adsorption energies as your classmates.

The project will count toward the “Achievements” grade, and will be graded based on the following:

**Midterm:**

-   5: Three adsorption energies reproduced to within 0.1 eV accuracy using the SPARC code.
    
-   4: Two adsorption energies reproduced to within 0.1 eV accuracy using the SPARC code.
    
-   3: One adsorption energy reproduced to within 0.1 eV accuracy using the SPARC code.
    
-   2: No adsorption energy successfully reproduced, but significant effort made.
    
-   1: No adsorption energy successfully reproduced, but some effort made.
    
-   0: No effort made.
    

**Final:**

-   5: A set of LLM prompts that can be used with ChatDFT (or any other LLM of your choosing) to automatically set up input scripts for an adsorption energy calculation, demonstrated on at least one of the 3 examples.
    
-   4: Discussion of a clearly defined research question or hypothesis, including evidence from your experience working with LLMs to reproduce adsorption energies. Some example research questions are provided below.
    
-   3: Three adsorption energies reproduced to within 0.1 eV accuracy using the SPARC code, and general commentary on how this was achieved.
    
-   2: Two adsorption energies reproduced to within 0.1 eV accuracy using the SPARC code, and general commentary on how this was achieved.
    
-   1: One adsorption energies reproduced to within 0.1 eV accuracy using the SPARC code, and general commentary on how this was achieved.
    
-   0: No adsorption energies successfully reproduced. Note that the accuracy threshold assumes that there are no major reproducibility issues with the examples you selected. In cases where significant reproducibility issues are discovered, then it is only necessary to show that your own adsorption energy calculations are converged to a numerical accuracy of 0.05 eV.
    

## Description:

### Phase 1: Reproduce at least three adsorption energies from the literature using the SPARC code.

This involves identifying three published adsorption energies from one or multiple papers of your choosing. Selecting different papers will be more challenging, but you will also learn more in the process. You should then use all information provided in the “Methods” and “Supplementary Material” (or other) sections of the publication to attempt to reproduce the adsorption energy using the SPARC DFT code. It is expected that the “numerical error” associated with this should be below 0.1 eV as long as there are no issues with the published results. More details are provided below.

### Phase 2: Using AI to enhance reproducibility.

In this phase, you will revisit the process of reproducing adsorption energy calculations and attempt to “formalize” it into a clear set of natural language prompts or instructions that can be used to have an AI model reliably reproduce the results. For the purpose of this project you only need to focus on reproducibility with the SPARC code, but as an additional challenge you can consider what would need to be modified to make it general to other codes.

We recommend first exploring the “ChatDFT” model for this process, but note that you are welcome to explore other alternatives that you have access to. If this process is successful, we are particularly interested in how it could be translated to a smaller LLM that could be run as a stand-alone inference model on a standard CPU. For those interested in LLM development, this may be an interesting question to pursue. Examples of other possible research questions are provided below.

## Suggested Workflow for Phase I:

A specific workflow of how to reproduce an adsorption energy is given below. You can consult ChatDFT or other LLMs along the way to help make these tasks more specific, and of course you can always ask an instructor if you aren't sure. You should make notes of any particular pain points along the way, which will be helpful in Phase II.

1) Identify adsorption energies in the literature. Find a paper that reports 3 or more adsorption energies, or find 3 papers with one adsorption energy each. In your biweekly update, include the citation(s) for the paper(s), the surface and adsorbate you will calculate (e.g. CO* on Pt(111)) , and the value you will seek to reproduce.

2) For each adsorption energy, identify the parameters that control the *physical accuracy* of the calculation. This includes the exchange-correlation (XC) functional used and the positions of the atoms involved (including slab thickness, how many atoms are fixed/relaxed, etc.). You can assume that these do not change, although if you want to be very rigorous the lattice constant may need to be adjusted since it can vary slightly due to numerical error. The XC functional should be stated in the methods section, but you may need to look harder to find the atomic positions and other detailed assumptions. In some cases, these may not even be explicitly provided, in which case it will be necessary to re-construct the slab model by optimizing the bulk structure and "cutting" the slab. Report these details in your biweekly update.

3) For each adsorption energy, identify the reported settings that control the *numerical accuracy* of the calculation. This includes the planewave cutoff or mesh spacing, the k-point density (number of k-points times the unit cell dimension), and  the convergence tolerances. In some cases, these details may not be reported. In others, they may differ from the exact settings available in SPARC. In these cases, discuss with a graduate student to make a decision about the "baseline" numerical settings to use. Report these details in your biweekly update.

4) Use the baseline numerical settings to compute the adsorption energies in SPARC. This should require ~3-5 individual DFT calculations per adsorpton energy: the bare slab, the slab+adsorbate complex, and the gas-phase molecule or gas-phase "references". If the "reference" is not the adsorbate molecule, then you will need to calculate the reference molecules in the gas phase. This can be very tricky, and there is a [detailed review paper here](https://pubs.rsc.org/en/content/articlehtml/2025/cs/d4cs00768a), or you can just ask an instructor to help you during class. In most cases, the "baseline" numerical settings should yield results within ~0.1 eV of the reported value.

5) If the values do not match to within 0.1 eV, perform troubleshooting to identify the problem. If the difference is larger than 1 eV, then something is very wrong. The most common culprit is the wrong "reference state" (typical errors are ~1-3 eV) or inconsistent numerical settings between slab/slab+ads/gas calculations (typical errors are ~1-10 eV or larger). If the difference is ~0.5 eV, then you should perform numerical convergence testing to ensure that your results are well-converged. This involves increasing the planewave cutoff/mesh spacing and k-point density to ensure that the result is well-converged.

6) (Optional) Attempt to improve the results by increasing the numerical accuracy of your calculation. The 0.1 eV tolerance is quite loose, and in general it should be possible to converge adsorption energies to within 0.03 - 0.05 eV, assuming both calculations are well-converged. You can increase the numerical settings of your calculation to determine it's numerical accuracy, and see if the agreement with literature gets better or worse as numerical errors are decreased.

## Research Questions for Phase II:

Phase II of the project involves original research, so there is not a standardized workflow to follow. The general goal is to establish a systematic way of writing instructions for calculating adsorption energies that ensures or improves reproducibility. The instructions above are a very rough starting point, but need to be supplemented with specific information about the system to reproduce (e.g. the information gathered in steps 1-3), and need to be revised to ensure that LLMs can reproduce them. 

Some specific research questions to consider:

1) What is the most difficult step to convey in natural language? How would reproducibility be improved if natural language is supplemented with specific data structures (e.g. .xyz files).

2) What information is missing from existing literature reports that make it difficult  to reproduce? Is it possible to write a "Methods" section that can be used along with some standard prompts to reproduce an adsorption energy?

3) Based on your experience, how would you revise the workflow for Phase I above to be easier to use? For example, you could provide specific prompts that LLMs were able to use to complete the tasks.

4) How does the size/complexity of the LLM used influence it's ability to help with reproducing the adsorption energies? Is it necessary to use an online model, or would it be possible to run an LLM locally that can reliably use a well-engineered set of prompts to calculate adsorption energies based on standard inputs?

5) What aspects of your experience with the LLM are specific to the SPARC code? How would the approach differ if you tried to use a different DFT code such as Quantum Espresso?

You should select or come up with a research question after the midterm and write it in your biweekly updates. Each update should then revise the question and/or provide evidence to help answer it.