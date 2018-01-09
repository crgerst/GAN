# GAN
experimentation with GANs

Training WGAN on 64x64 imagenet is really really slow!!!!  Gradient calculation may be causing the delay...need to check this out.


11/21:
Removing the momentum parameters from the Adam Optimizer appears to have a large negative impact on the output (as of the first step)

I compared the image in GAN/samples/imagenet/sample_199.png to the one which is where the new data samples are being stored, which is in improved_wgan_training/samples/imagenet/samples_199.png

Same conclusion on the 399 training step.

By doing nvidia-smi, I am seeing that I am using 98% of the GPU capacity for the wgan calculations!
