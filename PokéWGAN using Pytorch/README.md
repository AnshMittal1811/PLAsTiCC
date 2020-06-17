# PokéWGAN using Pytorch

This is the project created with reference to the work done by [Moxiegushi's PokéGAN](https://github.com/moxiegushi/pokeGAN) which was based on Tensorflow while this project utilizes Pytorch to do the same. Apart from this PokéGAN uses all of the sprites used till Pokémon generation 8 (which is based on Galar-based pokémon evolution families).

### Dataset
------

The complete dataset is contained within the `data` folder of the repository. The pokémon sprites for Pokémon generation 1 to generation 6 were taken from [Kaggle (from kvpratama)](https://www.kaggle.com/kvpratama/pokemon-images-dataset), for Pokémon generation 7 is from [Kaggle (from adityamhatre)](https://www.kaggle.com/adityamhatre/pokemon-transparent-images-dataset) and Pokémon generation 8 is from [Bulbapedia](https://bulbapedia.bulbagarden.net/wiki/List_of_Pok%C3%A9mon_by_evolution_family#Galar-based_evolution_families).

### Network Architecture
------
Here, we use WGAN (Wasserstein Generative Adversarial Networks) instead of the more common DCGAN (Deep Convolutional Generative Adversarial Networks) to account for Wasserstein loss. This loss function depends on a modification of the GAN scheme (called "Wasserstein GAN" or "WGAN") in which the discriminator does not actually classify instances. For each instance it outputs a number. This number does not have to be less than one or greater than 0, so we can't use 0.5 as a threshold to decide whether an instance is real or fake. Discriminator training just tries to make the output bigger for real instances than for fake instances.

Because it can't really discriminate between real and fake, the WGAN discriminator is actually called a "critic" instead of a "discriminator". This distinction has theoretical importance, but for practical purposes we can treat it as an acknowledgement that the inputs to the loss functions don't have to be probabilities. For more information, please refer [here](https://arxiv.org/pdf/1701.07875.pdf).

### Generation
------
The generation was originally set to 10000 epochs. This process was truncated due to Google colab going out of RAM which inadvertently stopped the process at 2621 epochs.

##### 64 Image Generation results after 2621 epochs
![64 Image 2621 epochs](https://github.com/AnshMittal1811/PytorchProjectsPortfolio/blob/master/Pok%C3%A9WGAN%20using%20Pytorch/Source/fake_images-2620.png "64 Image 2621 epochs")

##### 64 Image Generation results over 2621 epochs
Find the generation results over 2621 epochs over [here](https://youtu.be/tkRwoSm4AFA)


##### Single Image Generation during 2621 epochs
![1 Image 2621 epochs](https://github.com/AnshMittal1811/PytorchProjectsPortfolio/blob/master/Pok%C3%A9WGAN%20using%20Pytorch/Source/pokegans_generation_after_2600_epochs.gif "1 Image 2621 epochs")


##### 64 Image Generation results after 755 epochs
![755 epochs](https://github.com/AnshMittal1811/PytorchProjectsPortfolio/blob/master/Pok%C3%A9WGAN%20using%20Pytorch/Source/fake_images-0755.png "64 image Generation results after 755 epochs")


##### 64 Image Generation during 50 epochs
![50 epochs](https://github.com/AnshMittal1811/PytorchProjectsPortfolio/blob/master/Pok%C3%A9WGAN%20using%20Pytorch/Source/pokegans_training_50_epochs.gif "64 image Generation during 50 epochs")


### Real Image
------
![Real Image](https://github.com/AnshMittal1811/PytorchProjectsPortfolio/blob/master/Pok%C3%A9WGAN%20using%20Pytorch/Source/real_images.png "Real Image")
