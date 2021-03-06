# OpenSigns

## Installation

1. Create a conda enviroment with python 3.6.5 and activate it. \
`conda create --name sign_det python=3.6.5` \
`conda activate sign_det`

1. Install tensorflow 1.13.1 and tensorflow-gpu 1.13.1. It is crucial to install it both with pip and conda. \
`pip install tensorflow==1.13.1 --upgrade` \
`conda install tensorflow==1.13.1` \
`pip install tensorflow-gpu==1.13.1 --upgrade` \
`conda install tensorflow-gpu==1.13.1`

1. Install keras-retinanet 0.5.1.
   * Clone [keras-retinanet](https://github.com/fizyr/keras-retinanet) repository.  \
   `git clone https://github.com/fizyr/keras-retinanet.git`

   * Move to the keras-retinanet folder. \
   `cd keras-retinanet`

   * Create a branch from 0.5.1 and switch to it. \
   `git checkout -b branch0.5.1 0.5.1`

   * Install it. \
   `pip install . --upgrade`

1. Install keras-maskrcnn 0.2.2.
   * Clone [keras-maskrcnn](https://github.com/fizyr/keras-maskrcnn) repository. \
   `git clone https://github.com/fizyr/keras-maskrcnn.git`

   * Move to the keras-maskrcnn folder. \
   `cd keras-maskrcnn`

   * Create a branch from 0.2.2 and switch to it. \
   `git checkout -b branch0.2.2 0.2.2`

   * Install it. \
   `pip install . --upgrade`

1. Install keras 2.2.5. \
`pip install keras==2.2.5 --upgrade`

1. Install matplotlib with dependencies. \
`pip install matplotlib --upgrade`\
`conda install matplotlib`

1. Install exiftool. \
`sudo apt-get install exiftool`

1. Clone this repository. \
`git clone https://github.com/Jozko55/bike_signs_detection.git`

1. Download the [model](https://github.com/Jozko55/bike_signs_detection/blob/master/resnet50_final.h5) separately. \
You may need to adjust `PATH_TO_MODEL` in `script.py`.


## Usage

Firstly, create a folder where both input pictures and outputs will be stored. The folder must contain two separate folders named `inputs` and `outputs`. The subfolder `inputs` should contain your input pictures. The subfolder `outputs` should be empty.

Now, adjust accordingly the variable `path_to_data` in the file `script.sh`. (By default it is the path to `sample_data`.)

Finally, run everything. \
`./script.sh`

## Results

There will be exactly 4 output files generated for every detected bike sign on an input picture.

* `_mask.JPG`
* `_box.JPG`
* `_exif.json` (generated by exiftool from original picture)
* `_info.json` (name of detected sign and given score)



