# Fast MN UNet segmenter
This is a modernized version of the neural net used for live-cell identification and sorting of MN+ cells, as described in [doi:10.7554/eLife.101579.1](https://elifesciences.org/reviewed-preprints/101579). The original code used in the paper was based on FastAI 1.0. This is an updated library using FastAI 2.0.

## Installation
Install the necessary dependencies:
````
pip install -r requirements.txt
````

## Usage
Training data used for the paper are stored in training-data. You may train your own model following the Jupyter notebook `train-vcs`.

An useage example is provided in the `run-vcs` notebook. 

Note: optimizing the speed and performance of this library will depend on your particularly use case. You may need to adjust how nuclei are segmented, how crops are generated, or how predictions are assembled to suit your specific details.