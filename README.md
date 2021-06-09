# Experiments for the article "A Comparison of Neural Networks for Sign Language Recognition with LSA64" (JCC 2021) 

# How to run experiments

The notebooks in the models folder contain the code to run the experiments. Each notebook corresponds to each of the three architectures used in the paper. To run them you must first create a project structure in google drive. If you run the experiments in colab the first cell of the notebook will mount it in colab's virtual machine. 

We will call different variations of LSA64 as a "dataset". For example, resampling to 16 frames with data augmentation results in the Multisampling16 dataset. Resampling to 32 frames with no data augmentation results in SimpleSampling32 dataset. Although these variations can be generated for each batch during training, we saved them as videos in different folders to ease computation costs. 

## Project Structure 

The experiments were executed using colab by connecting it with google drive. You need to create a folder structure like the following

basePath/Experimentos/
basePath/Videos/
basePath/DatasetNames

basePath is were you will save all necesary files to reproduce the experiments

### Experimentos folder 

/Experimentos/ is were you will save experiments. If you are going to work with MobileNet, you should create a folder here named ' MobileNet+Conv '. If you will be working with the 'SimpleSampling32' dataset, you should create another folder inside ' MobileNet+Conv '. The result will be a path like this:

basePath/Experimentos/MobleNet+Conv/SimpleSampling32

This is the path where all experiments using MobileNet+Conv model with SimpleSampling32 dataset will be saved.

### Videos folder 

Here you will place folders containing Videos for each dataset. Below are the google drive links to the original folders. Create shortcuts to basePath/Videos/ folder with names indicated next to each link

* link: Originals
* link: SimpleSampling32

### DatasetNames folder 

Here you will place folders containing text files with names of different videos of a given dataset. These will be used by generators to select the videos to load for each batch. Below are the google drive links to the original folders. Create shortcuts to basePath/DatasetNames/ folder with names indicated next to each link

* link: Originals
* link: SimpleSampling32


# Supplementary materials
* Activation videos
  * [ConvLSTM]()
  * [MobileNet]()
  * [Conv3D]()

# Citation 

```
@inproceedings{mindlin2021lsa64,
  title={A Comparison of Neural Networks for Sign Language Recognition with LSA64},
  author={Mindlin, Ivan and Quiroga, Facundo and Ronchetti, Franco and Dal Bianco, Pedro and Rios, Gastón and Hasperué, Waldo and Lanzarini, Laura},
  booktitle={Not yet available},
  pages={},
  year={2021},
  organization={Universidad Nacional de La Plata}
}
```
