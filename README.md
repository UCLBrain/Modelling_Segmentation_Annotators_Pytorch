# Modelling_Segmentation_Annotators_Pytorch

# (This is a work in progress, a polished version would be released very soon.)

**The architecture of our model is depicted below:**

# Setup package in virtual environment
```sh
  - git clone https://github.com/UCLBrain/LearnNoisyLabels_Pytorch
  - cd LearnNoisyLabels_Pytorch/
  - conda env create -f conda_env.yml
```
# Download & preprocess the Brats dataset
<dl>
  <dd>(1) Download the training dataset with annotations from: https://www.med.upenn.edu/cbica/brats2019/registration.html
  <dd>(2) Unzip the data and you will have two folders: 
  <dd>(3) Extract the 2D images and annotations from nii.gz files by running
   
   ```sh
      - cd Brats
      - python Prepare_BRATS.py
   ```
# Training
<dl>
  <dd>(1) For Brats dataset, set the parameters in Test.py
   
   ```sh
      - input_dim=4,
      - class_no=4,
      - repeat=1,
      - train_batchsize=2,
      - validate_batchsize=1,
      - num_epochs=30,
      - learning_rate=1e-4,
      - alpha=1.5,
      - width=16,
      - depth=4,
      - data_path=your path,
      - dataset_tag='brats',
      - label_mode='multi',
      - save_probability_map=True,
      - low_rank_mode=False,
      - rank=0,
      - epoch_threshold=0,
      - alpha_initial=-1.5,
      - regularisation_type='2'
   ```
   <dd>(2) source activate env
   <dd>(3) python NNTrain.py
    
# Evaluation

**Below see testing samples from Brats dataset:**
 
# How to cite this code
Please cite the original publication:
