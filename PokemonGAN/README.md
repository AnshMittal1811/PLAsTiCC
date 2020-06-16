# PokeGAN using Pytorch

This is the project created with reference to the work done by [Moxiegushi's PokeGAN](https://github.com/moxiegushi/pokeGAN) which was based on Tensorflow while this project utilizes Pytorch to do the same. Apart from this PokeGAN uses all of the sprites used till Generation 8 (which is based on Galar-based evolution families).

### Dataset
The complete dataset is contained within the `data` folder of the repository. The pokemon sprites for Genertion 1 to Generation 6 were taken from [Kaggle](https://www.kaggle.com/kvpratama/pokemon-images-dataset), for Genertion 7 is from [lanpartis GitHub pokeGAN/POKEMON](https://github.com/lanpartis/pokeGANs/tree/master/POKEMON) and Generation 8 is from [Bulbapedia](https://bulbapedia.bulbagarden.net/wiki/List_of_Pok%C3%A9mon_by_evolution_family#Galar-based_evolution_families).


### Generation
##### 64 Image Generation during 50 epochs
![50 epochs](https://github.com/AnshMittal1811/PytorchProjectsPortfolio/blob/master/PokemonGAN/Source/pokegans_training_50_epochs.gif "64 image Generation during 50 epochs")

##### 64 Image Generation results after 755 epochs
![755 epochs](https://github.com/AnshMittal1811/PytorchProjectsPortfolio/blob/master/PokemonGAN/Source/fake_images-0755.png "64 image Generation results after 755 epochs")

##### Single Image Generation during 2600 epochs
![2600 epochs](https://github.com/AnshMittal1811/PytorchProjectsPortfolio/blob/master/PokemonGAN/Source/pokegans_generation_after_2600_epochs.gif "2600 epochs")


### Real Image
![Real Image](https://github.com/AnshMittal1811/PytorchProjectsPortfolio/blob/master/PokemonGAN/Source/real_images.png "Real Image")
