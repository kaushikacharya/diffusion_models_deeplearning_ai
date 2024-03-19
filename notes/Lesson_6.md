# Speeding Up

- Sampling is slow in DDPM because:
  - There are many timesteps.
  - Each timestep is dependent on the previous one (Markovian).

- Many new samplers address this problem of speed.
  - One of them is called DDIM
    - Denoising Diffusion Implicit Models

- Markov chains are only used for probabilistic processes.
- DDIM removes all the randomness from the sampling process, and is therefore deterministic.
- DDIM is faster because it skips timesteps.
- It predicts a rough idea of the final output and then refines it with the denoising process.

## Notebook

- [Jupuyter noteboook](../code/L4_FastSampling.ipynb)
- The same model can be used for both DDPM and DDIM.
  - As this is sampling process after training.
