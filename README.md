# LungSegmentation

This repository contains the model trained for segmenting MR lung images as described in:

Weng A et al. Deep learning-based segmentation of the lung in MR-images acquired by a stack-of-spirals trajectory at ultra-short echo-times. XXX 

The images used for training were exclusively acquired by a stack-of-stars UTE MR pulse sequence on a 3T Magnetom Prisma Scanner in healthy volunteers and patients suffering from cystic fibrosis.

The matlab-based CNN can be downloaded via the following link:

https://ukwde-my.sharepoint.com/:u:/g/personal/wech_t_ukw_de/EeRdW_enBQ5PgFqpcTlkbzoBS7j6M-9n6BG49aCTvPuBjw?e=BkImlx

Loading CNN.mat in matlab stores a variable named "net" in your memory.

Application of the network to obtain semantic segmentation in lung images works as follows:

C = semanticseg(repmat(lung_ima_2D,[1 1 3])),net);    % requires "Deep Learning Toolbox"

lung_ima_2D corresponds to a 2D UTE image of the lung of size [192, 192], formatted in uint8.

C is the resulting segmentation mask.
 
 


