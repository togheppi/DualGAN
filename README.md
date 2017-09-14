# DualGAN
PyTorch implementation of [DualGAN](https://arxiv.org/abs/1704.02510.pdf)
* Loss values are plotted using [Tensorboard in PyTorch](https://github.com/yunjey/pytorch-tutorial/tree/master/tutorials/04-utils/tensorboard).

## sketch-photo dataset
* Image size: 256x256
*

### Results (TBD)
* RMSProp optimizer is used. Learning rate = 0.00005, batch size = 1, # of epochs = 45:
* 6 resnet blocks used for Generator.

GAN losses<br> ( ![FF8900](https://placehold.it/10/FF8900/000000?text=+) : Discriminator A / ![AE0000](https://placehold.it/10/AE0000/000000?text=+) : Discriminator B <br> ![CD52A7](https://placehold.it/10/CD52A7/000000?text=+) : Generator A / ![2156C9](https://placehold.it/10/2156C9/000000?text=+) : Generator B <br> ![58BEE4](https://placehold.it/10/58BEE4/000000?text=+) : L1 loss A / ![319F92](https://placehold.it/10/319F92/000000?text=+) : L1 loss B ) | Generated images<br>(Input / Generated / Reconstructed)
:---:|:---:
<img src = 'horse2zebra_results/horse2zebra_DualGAN_losses_epochs_200.png'> | <img src = 'horse2zebra_results/sketch-photo_DualGAN_epochs_200.gif'>

* Generated images using test data

    |Sketch to Photo<br>1st column: Input / 2nd column: Generated / 3rd column: Reconstructed|
    |:---:|
    |![](horse2zebra_test_results/AtoB/Test_result_2.png)|
    |![](horse2zebra_test_results/AtoB/Test_result_11.png)|
    |![](horse2zebra_test_results/AtoB/Test_result_50.png)|
    |![](horse2zebra_test_results/AtoB/Test_result_112.png)|
    |![](horse2zebra_test_results/AtoB/Test_result_115.png)|
    |Photo to Sketch<br>1st column: Input / 2nd column: Generated / 3rd column: Reconstructed|
    |![](horse2zebra_test_results/BtoA/Test_result_14.png)|
    |![](horse2zebra_test_results/BtoA/Test_result_31.png)|
    |![](horse2zebra_test_results/BtoA/Test_result_68.png)|
    |![](horse2zebra_test_results/BtoA/Test_result_111.png)|
    |![](horse2zebra_test_results/BtoA/Test_result_140.png)|

### References
1. https://github.com/moono/GANs/tree/master/DualGAN
2. https://github.com/duxingren14/DualGAN
3. https://github.com/wiseodd/generative-models
