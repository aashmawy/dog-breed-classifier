# dog-breed-classifier
Classification of Dog Breeds using CNNs

In this project, you will learn how to build a pipeline that can be used within a web or mobile app to process real-world, user-supplied images. Given an image of a dog, your algorithm will identify an estimate of the canine’s breed. If supplied an image of a human, the code will identify the resembling dog breed.

## Instructions

Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip). Unzip the folder and place it in the repo, at location path/to/dog-project/dogImages.

Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip). Unzip the folder and place it in the repo, at location path/to/dog-project/lfw. If you are using a Windows machine, you are encouraged to use 7zip to extract the folder.

Donwload the [VGG-16 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG16Data.npz) for the dog dataset. Place it in the repo, at location path/to/dog-project/bottleneck_features.

Linux (to install with GPU support, change requirements/dog-linux.yml to requirements/dog-linux-gpu.yml):
conda env create -f requirements/dog-linux.yml
source activate dog-project
Mac (to install with GPU support, change requirements/dog-mac.yml to requirements/dog-mac-gpu.yml):
conda env create -f requirements/dog-mac.yml
source activate dog-project
NOTE: Some Mac users may need to install a different version of OpenCV

conda install --channel https://conda.anaconda.org/menpo opencv3
Windows (to install with GPU support, change requirements/dog-windows.yml to requirements/dog-windows-gpu.yml):
conda env create -f requirements/dog-windows.yml
activate dog-project
(Optional) If you are running the project on your local machine (and not using AWS) and Step 6 throws errors, try this alternative step to create your environment.

Linux or Mac (to install with GPU support, change requirements/requirements.txt to requirements/requirements-gpu.txt):
conda create --name dog-project python=3.5
source activate dog-project
pip install -r requirements/requirements.txt
NOTE: Some Mac users may need to install a different version of OpenCV

conda install --channel https://conda.anaconda.org/menpo opencv3
Windows (to install with GPU support, change requirements/requirements.txt to requirements/requirements-gpu.txt):
conda create --name dog-project python=3.5
activate dog-project
pip install -r requirements/requirements.txt
(Optional) If you are using AWS, install Tensorflow.

sudo python3 -m pip install -r requirements/requirements-gpu.txt
Switch Keras backend to TensorFlow.

Linux or Mac:
 KERAS_BACKEND=tensorflow python -c "from keras import backend"
Windows:
 set KERAS_BACKEND=tensorflow
 python -c "from keras import backend"
(Optional) If you are running the project on your local machine (and not using AWS), create an IPython kernel for the dog-project environment.

python -m ipykernel install --user --name dog-project --display-name "dog-project"
Open the notebook.
jupyter notebook dog_app.ipynb
(Optional) If you are running the project on your local machine (and not using AWS), before running code, change the kernel to match the dog-project environment by using the drop-down menu (Kernel > Change kernel > dog-project). Then, follow the instructions in the notebook.
