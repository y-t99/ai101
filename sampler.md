## Sampler

> [Stochastic Differential Equations and Diffusion Models - Sep 28, 2021](https://www.vanillabug.com/posts/sde/)
>
> [Complete guide to samplers in Stable Diffusion - June 30, 2023](https://www.felixsanz.dev/articles/complete-guide-to-samplers-in-stable-diffusion#stochastic-variants)
>
> [Stable Diffusion Samplers: A Comprehensive Guide - May 12, 2024](https://stable-diffusion-art.com/samplers/)
>
> [What are Noise Schedules in Stable Diffusion? - Jul 25, 2024](https://www.analyticsvidhya.com/blog/2024/07/noise-schedules-in-stable-diffusion/)

The sampler is responsible for carrying out the denoising steps.

To produce an image, diffusion model first generates a completely random image in the latent space. The **noise predictor** then estimates the noise of the image. The **predicted noise** is subtracted from the image. This process is repeated a dozen times. In the end, you get a clean image.

This **denoising process** is called **sampling** because diffusion model generates a new sample image in each step. The method used in sampling is called the **sampler** or **sampling method**.

### Series

> - some sampler’s names have a single letter "a", They are **ancestral samplers**. An ancestral sampler adds noise to the image at each sampling step. They are **stochastic** samplers because the sampling outcome has some randomness to it.
>   Be aware that many others are also stochastic samplers, even though their names do not have an "a" in them.
>   The drawback of using an ancestral sampler is that the image would not converge. Compare the images generated using Euler a and Euler below.
> - The samplers with the label "**Karras**" use the **noise schedule** recommended in the [Karras article](https://arxiv.org/abs/2206.00364).
> - The `SDE` ([paper](https://arxiv.org/abs/2011.13456)) variants use stochastic differential equations. Without going into further detail, using this type of differential equations allows to model the noise in a more sophisticated and accurate way, using information from previous steps, which in principle would generate **higher quality images in exchange for being slower**. Being stochastic, it never converges, so the higher the number of steps they do not offer higher quality, but rather more variations, just like ancestral samplers.

1. **Euler**

   1. Euler, often preferred for iterative testing because of its speed and efficiency.
   2. Euler a (ancestral), offer flexible control over the sampling process. 

2. **Heun** [more than a century ago]
   Heun is the perfectionist brother of Euler.

3. **DDPM (Denoising Diffusion Probabilistic Models)** [2020]
   It often preferred for iterative testing because of its speed and efficiency.

4. **DDIM (Denoising Diffusion Implicit Models)** [2020] [outdated]
   It often preferred for iterative testing because of its speed and efficiency. 
   Implements sampling from an implicit model that is trained with the same procedure as [Denoising Diffusion Probabilistic Model](https://hojonathanho.github.io/diffusion/), but costs much less time and compute if you want to sample from it

5. **DPM (Diffusion Probabilistic Models)**

   1. DPM-Solver (Diffusion Probabilistic Model Solvers) [2022]: A Fast ODE Solver for Diffusion Probabilistic Model Sampling in Around 10 Steps.

      > DPM-Solver support the following four algorithms: 
      >
      > - DPM-Solver, singlestep
      > - DPM-Solver, multistep
      > - DPM-Solver++, singlestep
      > - DPM-Solver++, multistep
      >
      > The all algorithms support orders contain 1, 2 and 3. DPM-Solver++ support the dynamic thresholding.
      > DPM-Solve++ 2M: DPM-Solver++, multistep, 2 orders.
      > DPM-Solver++ Karras: DPM-Solver++, multistep, thresholding (Karras).

   2. DPM-Solver++ (DPM2) [2022]: the DPM-Solver improved version.

   3. DPM-Solver++ Karras

   4. DPM-Solver++ a

   5. DPM++ SDE (Euler)

   6. DPM++ 2M SDE Heun Exponential

   7. DPM adaptive: it adjusts the step size adaptively.

6. **PLMS (Pseudo Linear Multi-Step)** [2021] [outdated]
   It often preferred for iterative testing because of its speed and efficiency. It is an improvement over DDIM. 

7. **LMS (Laplacian Pyramid Sampling)**
   LMS or Linear Multi-Step method is the cousin of PLMS that uses a numerical rather than a probabilistic approach (PLMS – P = LMS). It offers better accuracy in exchange for higher computational requirements (slower).

8. **UniPC (Unified Predictor-Corrector)** [2023]
   A Unified Predictor-Corrector Framework for Fast Sampling of Diffusion Models

### Component

1. Noise Schedule {Karras, Exponential, ... ... }
   Noise schedules play a crucial role in the steady diffusion process, dictating how noise is added and removed from data during both [forward](https://www.analyticsvidhya.com/blog/2024/07/forward-process-stable-diffusion/) and [reverse](https://www.analyticsvidhya.com/blog/2024/07/reverse-diffusion-process/) processes.
2. SDE (stochastic differential equation) Solver {Euler, Heun, ... ... }
   