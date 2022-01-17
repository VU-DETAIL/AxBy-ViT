# AxBy-ViT
AxBy-ViT: Reconfigurable Approximate Computation Bypass for Vision Transformers

## Required Python Packages
 - pytorch
 - pytorch-pretrained-vit
 - bitstring
 - PIL
 - numpy

## To run AxBy-ViT
 1. Install required packages.
 2. Prepare ImageNet dataset and put the inference set at ./val_imagenet. Each class must have its individual directories matching the synset names (as indicated in the python script)
 3. Initialize your GPU. By default GPU 0 is used.
 4. Configure approximate bypass settings by changing the argument of axby_config()
