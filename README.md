## View Adaptive Neural Networks(VA_NN)

This repo has been forked from the pytorch implementation of the View Adaptive Neural Networks for High Performance Skeleton-based Human Action Recognition, found here: https://github.com/jiamingNo1/VA_NN. This repo is for use as a submodule for the Lifelong Action Learning project (https://github.com/hwalli92/LAL-4-SARs)

### Prerequisites

* Python 3.6
* PyTorch 1.2
* Opencv 3.4
* Other packages can be found in ```requirements.txt```

### Data Preparation

Firstly, we need to download the [NTU-RGB+D](https://github.com/shahroudy/NTURGB-D) dataset.

Other Datasets: not supported now

* Extract the dataset to ```./data/NTU-RGB+D/nturgb+d_skeletons/```

* Process the data

`python data/ntu_generate_data.py`

Finally, we get the cross-view and cross-subject subsets for training, containing train, validate and test dataset seperately.

### Train

`python main_cnn.py` or `python main_rnn.py`

### Test

`python main_cnn.py --mode test` or `python main_rnn.py --mode test`

### Reference

[paper links](https://arxiv.org/abs/1804.07453)
