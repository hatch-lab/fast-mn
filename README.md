# Fast MN UNet segmenter
This is a modernized version of the neural net used for live-cell identification and sorting of MN+ cells, as described in [doi:10.7554/eLife.101579.1](https://elifesciences.org/reviewed-preprints/101579). The original code used in the paper was based on FastAI 1.0. This is an updated library using FastAI 2.0.

## Image information
Full field raw images of RPE1 cells expressing H2B-emiRFP703 after 24 h treatment with Mps1i used for testing are in the "full-field" folder. Three-channel image crops used for training of the same cells are in the "all" folder and comprise single nuclei segmented by RetinaNet. The channels are H2B-emiRFP703, H2B-emiRFP703, Sobel filter. Three-channel image crops used for testing are in the "test" folder.

Ground truth labels of micronuclei for "all" image crops are in the "annotations" folder.

## Installation
Install the necessary dependencies:
````
pip install -r requirements.txt
````

## Usage
Training data used for the paper are stored in training-data. You may train your own model following the Jupyter notebook `train-vcs`.

An useage example is provided in the `run-vcs` notebook. 

Note: optimizing the speed and performance of this library will depend on your particularly use case. You may need to adjust how nuclei are segmented, how crops are generated, or how predictions are assembled to suit your specific details.
