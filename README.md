# iGPT-notebook
Intuitive image-GPT notebook designed to use in google colab combined with free GPU. The project uses pretrained weights and model open-sourced by OpenAI. 

The improvements over original repo:
* simple hyperparameters choice via sliders etc. rather than command line
* adding the option of completing cropped image

# Usage
## 1) Click the link
First of all click this link : [iGPT-notebook](https://colab.research.google.com/drive/1hv7W9AHl7cRAwBp3NVhn3dfpH3Db9mWO?usp=sharing)

Make sure you go to `Runtime`, then `Change runtime type` and set the hardware accelerator to `GPU`. 

## 2) Clone the repo and install dependencies
Just simply click the run button it will copy this repo and install correct version of tensorflow to run the model.
![](https://github.com/maciejbalawejder/iGPT-notebook/blob/main/clone.png)

## 3) Load the model
The recommended settings are:
- batch 4 (the number of generated images or completions)
- model size s (different sizes seem to have worse completion capabilities)
- number of gpus 1 (under the hood you can change it but since we use one gpu provided by google colab I set it as a constant)
![](https://github.com/maciejbalawejder/iGPT-notebook/blob/main/model.png)

## 4) Load the image
To load and crop desired image, you need to drop it on the google cloud disk on the left sidebar. Then put the name in the `IMAGE_NAME` space. `CROP_N_PX` defines how many pixels are cropped from the bottom and can be manually adjusted. Keep in mind, all the images are rescaled to the 32x32 size. If you want to save the progression of the images, tick the `SAVE_IMAGE`. 
![](https://github.com/maciejbalawejder/iGPT-notebook/blob/main/load_image.png)

## 5) Generate images/completions
Run the cell to get the desired output. Tick `SAVE_RESULTS_PLOT` to keep the outputs. They all will be saved at the google colab disk on the left sidebar.
![](https://github.com/maciejbalawejder/iGPT-notebook/blob/main/generate.png)
