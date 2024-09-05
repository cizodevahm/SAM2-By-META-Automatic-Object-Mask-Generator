# SAM2-By-META---Automatic-Object-Mask-Generator
This repository demonstrates the use of **SAM2 (Segment Anything Model 2)** to automatically generate object masks for images. SAM2 efficiently processes prompts to generate masks by sampling over the entire image and predicting multiple masks from single-point input prompts. 

## Overview

The class `SAM2AutomaticMaskGenerator` implements the automatic mask generation capability by:
- Sampling single-point input prompts in a grid over the image.
- Predicting multiple masks from each point.
- Filtering masks using quality metrics and deduplication techniques like non-maximal suppression.
- Offering additional options to improve mask quality through multiple image crops and postprocessing to remove small disconnected regions and holes.

This notebook can run both locally and in Google Colab, with optimizations for GPU use.

## Installation

### Local Installation

To run the SAM2 model locally, first clone the repository and install the required dependencies:

```bash
git clone https://github.com/facebookresearch/segment-anything-2.git
cd segment-anything-2
pip install -r requirements.txt
```

## Usage
Once the environment is set up, you can use the ```SAM2AutomaticMaskGenerator``` class to automatically generate masks for any given image. The generated masks will be filtered for quality and deduplicated for efficient processing.

## Pretrained Models
The SAM2 model can use pretrained weights for generating object masks. Download the model checkpoint from the link below and place it in the appropriate directory:
- [SAM2 Large Model Checkpoint](https://dl.fbaipublicfiles.com/segment_anything_2/072824/sam2_hiera_large.pt)

## License
This project is licensed under the MIT License.
