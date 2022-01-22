# AxBy-ViT
AxBy-ViT: Reconfigurable Approximate Computation Bypass for Vision Transformers

## Required Platform
 - GPU with CUDA support

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
 4. Configure approximate bypass settings by changing the argument to the function **axby_config()**

## To-do
 1. Refraction.
   - A helper for enabling trivial bypass operation counting.
   - Replace hardcoded filler number with dynamic allocations.
   - synset names into an external file.
 2. Feature Additions
   - Allow user to directly configure the mantissa bits of semi-trivial bypass.
   - Allow running the framework without a GPU.
   - Allow the configuration of AxBy-ViT via commandline argument.
 3. (Overhaul) Directly manipulating on original transformer object rather than defining custom classes.
   - Currently using new classes inherited from the original transformer class for legacy designing issues however this can be avoided since pytorch already provides interface.
   - This require an OOP re-implementation of AxBy-ViT 
