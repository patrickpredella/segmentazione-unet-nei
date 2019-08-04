# Segmentazione di immagini di Nei con U-Net Convolutional Neural Network

1. Conda env details in environment.yml

```
conda env create -f environment.yml
conda activate tensorflow_env
jupyter notebook
```

2. Copy dataset in dataset folder
3. Extract training and ground truth images keeping the original folder names

./dataset/Dataset_Nei/Segmentazione/ISIC2018_Task1-2_Training_Input
./dataset/Dataset_Nei/Segmentazione/ISIC2018_Task1_Training_GroundTruth

4. Run 01_dataset_compressor.ipynb in a jupyter notebook.<br/>This will create a compressed copy of the dataset based on the specified resolution
5. Run 02_UNet-Segmentation-Trainer.ipynb in a jupyter notebook.<br/>This will train the U-Net based on the parameters specified in the hyperparameters section and output the weights of the U-Net in the file UNetW-[img_size]. Increase epoch count to train the Unet for more iterations, tune batch size for performance/memory.
6. Run 03_UNet_Executor.ipynb in a jupyter notebook.<br/>This will execute the U-Net using the "Validation" dataset and the computed weights.

