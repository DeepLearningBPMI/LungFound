# LungFound
A foundational model for OCT lung images that uses a masked autoencoder based on the vision transformer architecture.

The original repository and most files were obtained from [RETFound](https://github.com/rmaphoh/RETFound_MAE/tree/main).
Some adjustments have been made to the files compared to the RETFound repository. 

To use an MAE, pre-train it on (unlabelled) data with main_pretrain.py. 
LF_visualize.ipynb visualizes the reconstruction process of the images of the MAE and can be compared with how well it performs in reconstruction.

main_finetune.py refines the pre-trained weights obtained after main_pretrain.py.
An example of how the labelled data must be formatted in the labelled datafolder is shown in the fine-tune-datafolder-ex folder.

LF_Dim_reduction creates PCA and t-SNE plots (2 and 3 components) to gain insight into their separation performance of image classes in the latent space. 

The images are not required to be in (224, 224) format. However, they must be in RGB format (i.e. (224, 224, 3). 
For gray-scale images to be formatted in RGB, the pixel values need to be repeated in the three colour channels.
