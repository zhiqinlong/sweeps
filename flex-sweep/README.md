########flex-sweep demonstrates robustness to demographic misspecification as well as recombination rate heterogeneity and background selection. Despite this, its performance suffers when trained under a very different demographic scenario (e.g., expansion) than the true history (e.g., decline). The whole- genome sequence data with good depth of coverage needed to find sweeps also allow demographic inference. So in this circumstance, it would be beneficial to infer the general trend of the population history using the available data and a method such as ∂a∂i, PSMC , MSMC , Relate , or StairwayPlot2 and use the resulting inferred demographic model for Flex-sweep training simulations. Flex-sweep has good power to detect sweeps at FPRs of less than 1% in simulations, though this is reduced by background selection. Moreover, although this method does require knowledge of derived and ancestral alleles, it is not dependent on having an outgroup sequenced population nor admixture within the population being studied. (M Elise Lauterbur, Kasper Munch, David Enard, Versatile Detection of Diverse Selective Sweeps with Flex-Sweep, Molecular Biology and Evolution)

##fisrt step training simulating your own model based on the real demographic history.

###enviroment requirement 
#####module load StdEnv/2020 python/3.9.6 scipy-stack 
#####pip install psutil joblib tensorflow==2.8 scikit-allel
####install discoal 
git clone https://github.com/kr-colab/discoal.git
discoal has hard coded a limit on the number of sites allowed to be simulated to 220020. If the user wishes to simulate larger regions they will need to change the MAXSITES define in discoal.h and recompile (change 220020 to 1220020). because the window size is 1.2M for flex-sweep.
make
####run simulate command

