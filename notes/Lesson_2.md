# Sampling

- Normalizing by $1/\sqrt{2}$ after adding residual
  - [Stackexchange thread](https://stats.stackexchange.com/questions/553634/understanding-normalisations-in-stylegan2-and-on-general) attempts an explanation
    - Variance increases on addition of random variables.
    - Explains that if variance of both random variables are same then that out lead to dooubling of variance which woould in turn lead to gradient explosion when there are multiple layers.

## [Notebook](../code/L1_Sampling.ipynb)

- [matplotlib.axes.Axes.set_xticks](https://matplotlib.org/stable/api/_as_gen/matplotlib.axes.Axes.set_xticks.html) should be used in place of `set_ssticks`. Similarly for y.
- Observation:
  - For random noise added to the sampling, we should use `torch.randn_like`. This generates random numbers from standard normal distribition. By mistake I used `torch.rand_like` which generates random numbers from standard uniform distribution. That failed to generate sprite images.
- Sampling output: Generating sprites from noise
  - ![Sampling animation](../code/weights/ani_run_wNone.gif)
