# Single-particle dynamic analysis
This Jupyter notebook contains Python functions designed to calculate and plot key performance metrics of micron-scale DNA motors driven by RNase H. The tools are also applicable to other dynamic systems operating at the nanoscale or microscale with 2D motion.

## 1. "Medusa" plot
By tracking the positions of individual microparticles on a planar surface using optical microscopy, we obtain a time series of (x, y) coordinates, typically stored in a CSV file. These coordinates can be used to reconstruct single-particle trajectories, which are often visualized as color-coded lines, with color indicating the timepoint within the timelapse video. 

When trajectories from a population of motors are overlaid in a single diagram and centered at (0,0), the resulting visualization, which resembles a cluster of tentacle-like paths, is often referred to as a "medusa" plot.

![image](https://github.com/user-attachments/assets/2f35ee3a-508c-4c14-85d0-d42d370d0a13)

## 2. Net Displacement
Net displacement refers to the straight-line distance and direction from an object's starting position to its final position, regardless of the path taken.

<img width="495" alt="Screenshot 2025-06-14 at 7 27 49 PM" src="https://github.com/user-attachments/assets/94cbd49c-5d54-463a-8a0e-8e0feac2efee" />

It gives a measure of how far, and in what direction, the particle has moved overall during the observation period.
This is distinct from total distance traveled, which sums the entire trajectory traveled.

## 3. Mean Square Displacement
Mean Square Displacement (MSD) is a statistical measure used to quantify the average squared distance a particle travels over time. It is widely used in fields like biophysics, soft matter, and materials science to characterize the motion of particles—especially in diffusion or motor-based transport.
<img width="645" alt="Screenshot 2025-06-14 at 7 34 13 PM" src="https://github.com/user-attachments/assets/ed2a2deb-2f5d-4cc5-8379-21631e3049c7" />

## 4. Alpha diffusional coefficient
One parameter to quantify the super-diffusive nature of DNA motors is the power law dependence between the mean square displacement (MSD) and the lag time τ. 

<img width="90" alt="Screenshot 2025-06-14 at 7 42 25 PM" src="https://github.com/user-attachments/assets/d1ff80c6-9543-48e6-b3f4-55f07de03806" />

The scaling exponent α (alpha) gives a value of 1 for random Brownian diffusion (linear dependence), <1 for sub-diffusive motion, and >1 for super-diffusive motion. This diffusional coefficient is also an excellent indicator of motor processivity as detachment from the track abolishes the self-avoiding bias.
