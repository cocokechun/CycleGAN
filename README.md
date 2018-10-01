# CycleGAN

Image-to-image translation is a fun topic. Classic examples are like turning an image of a horse to an image of a zebra. More useful example can be turning a black-and-white image to a colored image.

Good thing is that, for people to experiment with image-to-image translation, there're many libraries or code bases in which people implement classic models and everyone can use those to experiment.

The first classic image-to-image library is pix2pix. I tried this git repo (https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix) because it's implemented by the original author of Image-to-Image Translation with Conditional Adversarial Networks and CycleGAN.

pix2pix requires paired images for training. The dataset they provide are like Yosemite summer to winter, facade map to real facade image. You can also try to make your own dataset by following [instructions](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix/blob/master/docs/datasets.md). You just need to provide 2 folders, and images with the same in 2 folders will be paired by the script. pix2pix is not crazy slow. 400 facade image pairs can generate reasonable results within a few hours (with a local Mac laptop).

However, in reality, paired image dataset is not very easy to find. That's where CycleGAN came from. CycleGAN can do image-to-image translation provided 2 unordered sets of images to train. For example, one folder can purely contain horse images, and the other folder can purely contain zebra images. After training, CycleGAN can change a horse to zebra in the image (while keeping all other things roughly the same).

I was really interested in trying how good CycleGAN translate. I started with this [codebase](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix/blob/master/docs/datasets.md) mentioned above. However, the visualization tool doesn't show any visualization even after 2 or 3 hours (versus pix2pix started showing somehting within minutes).

Then I thought, perhpas the model implemented by tensorflow could be faster.



