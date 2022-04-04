# Protocol adaptive STL Unet
STL Unet : Stacked transfer learning Unet

### File description
'enviornment.yml' : Enviornment file for recreating the conda enviornment

`data.py` : Create generators for training and testing, other utility functions

`model.py` : Tensorflow model of the Unet and loss functions

`Three level tranfer learning.ipynb` :  This notebook trains the protocol adaptive STL Unet with the different datasets

`There level optimization.ipynb` : Optimization notebook allows you to select the best number of layers and other parameters to tune for a specific dataset. 

*Note* : This code is not needed to test the given data. Use it only if you want to test the model on a new dataset. Tuned parameters are already provided for the given datasets.


### How to use the code ( Steps )
1) Download the pretrained model and dataset using the link
2) Download the github Protocol adaptive STL Unet
3) Setup conda enviornment using the enviornment.yml file given in the repository
4) Open `Three level transfer learning.ipynb` file,

    1)  We have given three datasets : Storm, Radial and USC
    2)  Give Params = Storm/ Radial / Storm according to your wish.
    3)  Go forward with training the model
    4)  Best model ( based on best val loss ) will be saved to the specific location
    5)  Run the test and extract the test results.

5) For using custom datasets,
    1) Create folder structure similiar to any of the three given datasets with segmentations.
    2) we are using [weights and bias](https://wandb.ai/site) for tuning.
    3) Please sign up for free and use this [tutorial](https://docs.wandb.ai/quickstart) to setup W & B on your conda enviornment
    4) Once setup is done provide entity as your userID in the code.
    5) run the code with the W & B setup and it will generate a dashboard with the sweep details
    6) Once the sweep is finished download the excel sheet from the W & B dashboard to get the list of best parameters.
    7) Use that parameters in the `Three level tranfer learning.ipynb` to run your custom model


If you are using our code for your research Please cite 

[1]: S. Erattakulangara and S. G. Lingala, "Airway segmentation in speech MRI using the U-net architecture," 2020 IEEE 17th International Symposium on Biomedical Imaging (ISBI), 2020, pp. 1887-1890, doi: 10.1109/ISBI45749.2020.9098536.

[2]:Erattakulangara, S., and Lingala, S.G. U-net based automatic segmentation of the vocal tract airspace in speech MRI. " 2019 international society for magnetic resonance in medicine "

