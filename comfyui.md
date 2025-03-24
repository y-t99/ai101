## Model

> refer: [comfyui - models](https://docs.comfy.org/essentials/core-concepts/models)

The word ***model*** has many different meanings. Here, it means a data file carrying information that is required for a node graph to do its work. Specifically, it’s a data structure that *models* some function. As a verb, to model something means to represent it or provide an example.

model type: **Checkpoint**, **LoRA**, 

- A `checkpoint` usually contains three components: `MODEL (UNet)`, `CLIP`, and `VAE`

  - `CLIP`

    [A History of CLIP Model Training Data Advances - March 13, 2024](https://voxel51.com/blog/a-history-of-clip-model-training-data-advances/)
    Contrastive Language Image Pretraining (CLIP): a technique for bridging the gap between visual understanding and natural language understanding.
    [Introduced by OpenAI](https://openai.com/research/clip) in 2021, CLIP aligns a vision encoder and a text encoder so that the vision encoder’s representation of a photograph of a dog is similar to the text encoder’s representation of "a photo of a dog"

  - `VAE`
    [What is a variational autoencoder?](https://www.ibm.com/think/topics/variational-autoencoder)

    Variational autoencoders (VAEs) are [generative models](https://www.ibm.com/topics/generative-ai) used in [machine learning](https://www.ibm.com/topics/machine-learning) (ML) to generate new data in the form of *variations* of the input data they’re trained on. In addition to this, they also perform tasks common to other autoencoders, such as denoising.
    VAEs encode a *continuous*, probabilistic representation of that latent space. This enables a VAE to not only accurately reconstruct the exact original input, but also use variational inference to generate new data samples that resemble the original input data.


