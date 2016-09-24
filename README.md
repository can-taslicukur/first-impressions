# first-impressions
The repository contains code, documentation of the code used in ChaLearn First Impressions Analysis challenge

###ChaLearn LAP. Apparent Personality Analysis: First Impressions

used OS: Ubuntu 14.04

####Prerequisites for execution:


#####To extract audio features:


1. install ffmpeg
https://git.ffmpeg.org/gitweb/ffmpeg.git
(or)
try "sudo apt-get install ffmpeg"

2. python 2.7 (<--tested) (or above) 

######additional packages needed:

```
pip install --user eyed3
pip install --user mlpy
pip install --user scikit-learn
pip install --user progressbar
```

3. spftware installations for preparing OpenFace executable
Installation: https://github.com/TadasBaltrusaitis/OpenFace/wiki/Unix-Installation

   - make sure that open face is installed in the folder "OpenFace" of same directory of test files
   i.e., open face should be built and the file "FeatureExtraction" should 
   be available in the folder "data/OpenFace/build/bin"

5. Torch7
Installation: http://torch.ch/docs/getting-started.html


>important modules of Torch7:
>nn, cunn, cutorch, nngraph, rnn, image, optim, xlua, io
>CUDA 7.0 or above


###EXECUTION PROCEDURE:

####Preprocessing steps:

1. To start preprocessing of data, execute the below command

```
python setup.py
```

After preprocessing, there will be 4 new folders created under "data" folder namely,

   "data/trainaudiofeat" - training audio features
   "data/validationaudiofeat" - validation audio features
   "data/trainframes" - training video features
   "data/validationframes" - validation video features
   
2. To train the model,
--------------------------

--> in commandline, go to "src" folder,
--> execute "th doall.lua"

