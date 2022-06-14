# GAN for fashion-MNIST, with FID,Cuda
Attached is a basic GAN, referenced to "MNIST FASION".

Since the discriminator also improves during training, I needed an *external tool* to evaluate the improvement of the genreted images.

To do this I used FID.

https://en.wikipedia.org/wiki/Fr%C3%A9chet_inception_distance

Following are few pictures to illustrate the training progress.

Generated fake images.

![Epoch#0](https://github.com/anubhavanand1516/MSRF_GAN/blob/main/samples/fake_images-11.png)

Generated Real images.

![Epoch#3](https://github.com/anubhavanand1516/MSRF_GAN/blob/main/samples/real_images.png)


This GAN suffers from mode-collapse. 

By using an *Unrolled GAN*, we can prevent the generator from optimizing for a single fixed discriminator, since the loss function incorporates not only the current discriminator's classifications, but also future discriminator versions.

So the generator can't over-optimize for a single discriminator.

## Getting Started
Clone the repository into a local machine using
```shell
git clone https://github.com/anubhavanand1516/MSRF_GAN
```
### Instructions to run
These notebooks were developed on pytorch with cuda implementation, as they provide sufficient GPU resources to develop these models. To open these notebooks locally, run
```shell
python Teamx.py
```

Following is the FID graph:

![FID loss vs Epochs](https://user-images.githubusercontent.com/41025885/131232734-1f2bf977-dd45-4a65-8e28-38a8056d98cb.png)

Thanks.
