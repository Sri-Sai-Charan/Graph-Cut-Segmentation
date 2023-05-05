# Graph-Cut-Segmentation
As applied in the field of computer vision, graph cut optimization can be employed to efficiently solve a wide variety of low-level computer vision problems, such as image smoothing, the stereo correspondence problem, image segmentation, object co-segmentation, cv problems that can be formulated in terms of energy minimization. 

## Overview

Let us apply Graph-cuts for foreground/background segmentation. In the “cat” image, you are given a rough polygon of a foreground cat. Apply graph-cut based method to see if we can get a better segmentation!

Firstly, use the provided polygon to obtain an estimate of foreground and background color likelihood. You may choose the likelihood distribution (e.g., color histograms or color mixture of Gaussians.).

Secondly, apply graph-cut code (cv2.grabcut) to do better segmentation. You can use the provided bounding-boxes and use "cv2 package" for the implementation sake. You are required to draw interesting conclusions on how it performs on different samples.

## Usage

```
Run GraphCut.ipynb in Jupyter Notebook or Google Colab
```

# Results

<table>
  <tr>
    <td> <img src="Results/og_img.png"  alt="1" width = 360px height = 640px ><p align='center'> Original Image </p></td>
    <td><img src="./Results/gauss.png" align="right" alt="4" width = 360px height = 640px> <p align="center"> Gaussian Mixture Model</p> </td>
    
   </tr> 
   <tr>
      <td><img src="Results/fg_p_map.png" alt="3" width = 360px height = 640px><p align="center">Foreground Probability Map</p></td>
      <td><img src="Results/bg_p_map.png" alt="2" width = 360px height = 640px> <p align="center">Background Probability Map</p></td>  
  </tr>
    <tr>
        <td><img src="Results/fg_mask.png" alt="3" width = 360px height = 640px><p align="center">Foreground Mask</p></td>
        <td><img src="Results/eg_r.png" alt="2" width = 360px height = 640px> <p align="center">Result</p></td>
    </tr>
</table>


# Folder Structure
```
📦Graph-Cut-Segmentation
 ┣ 📂Results
 ┃ ┣ 📜bg_p_map.png
 ┃ ┣ 📜eg_r.png
 ┃ ┣ 📜fg_mask.png
 ┃ ┣ 📜fg_p_map.png
 ┃ ┣ 📜gauss.png
 ┃ ┗ 📜og_img.png
 ┣ 📜.gitignore
 ┣ 📜GraphCut.ipynb
 ┣ 📜LICENSE
 ┗ 📜README.md
```



