# Using Markov Chain Monte Carlo to Produce Bed Realizations of Scott Glacier
Part of a larger project to map subglacial topography to quantify the uncertainty in sea level rise predictions.

![Figure showing the progression of subglacial topography from bedmachine, sgs, and both MCMC chains](Figures/BedCompilation.png)

![Figure showing the variograms for each step of the process and the conditioning bed](Figures/BigVariogram.png)

The bed topography beneath glaciers and near their grounding line (not pictured), can greatly affect their flow and retreat dynamics. As such, we need to determine just how variable these sub-glacial topographies can be in order to predict the impact of glacial melting on sea level rise based on a variety of climate projections.

# Methods
We use Tutorial 1 (No tutorials present yet) to isolate our study area from bedmap, a database for Antarctic topographical data, by converting geographic coordinates to polar stereographic and establish a region of high velocity for future operations. We use Tutorial 2 to create a Sequential Gaussian Simulation (SGS) realization of the subglacial topography based on a matern variogram of our normalized bed. Tutorial 3 uses this SGS bed to run many large-scale Markov Chain Monte Carlo (MCMC) iterations constrained to certain physical and topographical constraints in order to produce many realizations with decreasing loss. One such physical constraint is mass conservation, which pushes the simulation to have a total mass loss and mass gain equal to a known value. The topographical constraints require areas with radar measurements or above-ground regions to match the data. Tutorial 4 continues with the small-scale MCMC, keeping the afformentioned constraints and iteratively changing small portions of the previous step using SGS to further minimize loss.

# Poster

![Placeholder image of a poor poster](Figures/PosterDraft.png)

# Target Audience
![pretty penguin](Figures/images.jpg)
