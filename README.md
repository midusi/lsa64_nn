# Experiments for the article "A Comparison of Neural Networks for Sign Language Recognition with LSA64" (JCC 2021) 

# How to run experiments

The notebooks in the models folder contain the code to run the experiments. Each notebook corresponds to each of the three architectures used in the paper. To run them you must first create a project structure in google drive. If you run the experiments in colab the first cell of the notebook will mount it in colab's virtual machine. 

Notebooks save intermediate results where in the experiment folder. That way, if training is interrupted it automatically starts where it left off

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

* https://drive.google.com/drive/folders/18wSLOpvFROn0q5tYD2fw4eXhnmnN7AHq?usp=sharing Originals
* https://drive.google.com/drive/folders/1Ce2mK3KGMMnN32fo4cs3XP66OVN8XlYo?usp=sharing SimpleSampling32
* https://drive.google.com/drive/folders/1JJCmRVPzGdcTGetBqpKmikyUqp2fDlRQ?usp=sharing Multisampling32
* https://drive.google.com/drive/folders/15jbkcFmaZYKTUcnx4Ctl3uKFOgotAWxq?usp=sharing Multisampling16
* https://drive.google.com/drive/folders/1Ly859ve6d63OgyPafckZhDE0cYFUrN9x?usp=sharing Multisampling8
* https://drive.google.com/drive/folders/1yFUFMrjOv5MeHsadxGw_AG0mdU2gXyL1?usp=sharing HSV

### DatasetNames folder 

Here you will place folders containing text files with names of different videos of a given dataset. These will be used by generators to select the videos to load for each batch. Below are the google drive links to the original folders. Create shortcuts to basePath/DatasetNames/ folder with names indicated next to each link

* https://drive.google.com/drive/folders/1_VvM9xip3vYs6UbM77nu2vk7S5A4c_tb?usp=sharing SimpleSampling32
* https://drive.google.com/drive/folders/1mQvhmGsjxd0JLTVwEa4e7xyunmGQrnr6?usp=sharing Multisampling32
* https://drive.google.com/drive/folders/1bX3CFuSrqyBhDeM_CAdpWnLU_pbe5xJk?usp=sharing Multisampling16
* https://drive.google.com/drive/folders/1z6tbJ12xjB7Sp-ehnAol_EPW2o095WAJ?usp=sharing Multisampling8


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
