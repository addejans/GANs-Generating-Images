# GANs-Generating-Images
Generating Images using GAN's

## Data Sets Used
 1. MNIST Handwritten Digits
 2. Fashion MNIST
 
---

# GAN Overview
 - GANs work by having a generator network (counterfeiter) who is being trained to create fake dollars that are indistinguishable from the real ones (generated by the bank).
 - The discriminator network (police) is being trained to determine if the money is real or fake.
 - The counterfeiter is trying to fool the police by pretending that he generated a real dollar bill.
 - However, the discriminator will detect the fake money and provide feedback to the generator on why he thinks that the money is fake. Overtime, the generator will become expert in generating new money that are indistinguishable from the real ones and the discriminator will fail to tell the difference.

## Build Generator
 - The generator takes in a random noise signal and output images.
 - The generator is trying to generate fake images that are similar to the real images (ones that comes from the training data)
 - The objective of the generator is to fool the discriminator.
 - Labels are marked as follows:
   - Label = 1.0 indicates real images
   - Label = 0.0 indicates fake images
 - The generator uses `tf.keras.layers.Conv2DTranspose` (upsampling) layers to create an image from a seed of noise.
 - The seed is fed to a Dense layer and upsampled several times (in our case, until the final image size of 28x28x1 is achieved).

## Build Discriminator
 - The discriminator is a basic Neural Network that is trained to perform classification task
 - The discriminator is trained to do the following:
   - Output 0 (probability = 0%) when the input image is fake
   - Output 1 (probability = 100%) when the input image is real

---

## //ToDo Eventually:
 - upload images of my own face for a truly unique project
