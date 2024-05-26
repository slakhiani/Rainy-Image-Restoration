# Rainy Image Restoration
This project is a Novel Deep Learning Architecture for the task of Image Deraining as a segment of image restoration. This project was for Capstone in Summer 2023.

The architecture is inspired by a hybrid of these approaches:
- Restormer: Efficient Transformer for High-Resolution Image Restoration  - https://arxiv.org/pdf/2111.09881.pdf
- Swin Transformer: Hierarchical Vision Transformer using Shifted Windows  - https://arxiv.org/pdf/2103.14030

<br>

## Dataset

[Rain100L](https://mega.nz/file/MpgnwYDS#jqyDEyL1U9srLBbEFCPnAOZb2HZTsSrwSvRGQ6m6Dzc) and [Rain100H](https://www.dropbox.com/s/kzbzer5wem37byg/rain100H.zip?dl=0) are used.
Rain 100H consists of 1800 high quality images with a resolution of 1200 x 900.
Rain 100L consists of 200 low quality images with a resolution of 200 x 200. 

<br>


## Model Evaluation

Peak-Signal-to-Noise Ratio (PSNR) and Structural Similarity (SSIM) were the two evaluation metrics selected for this project. PSNR measures the peak error between the original and derained images in terms of signal-to-noise ratio. PSNR was used over Mean Squared Error (MSE) because it normalizes for images encoded using different numbers of bits, it is more concise due to the log function, and because it is widely used in the industry. SSIM evaluates the structural similarity between the original and derained images in terms of luminance, contrast, and structure. A low PSNR and high SSIM indicate high model performance.

<br>

## Benchmarks

<table>
<thead>
  <tr>
    <th rowspan="1">Model</th>
    <th colspan="2">Rain100L</th>
    <th colspan="2">Rain100H</th>
    <th rowspan="1">Download</th>
  </tr>
  <tr>
  <td align="center">SwinStormer</td>
    <!-- <td align="center"></td> -->
    <td align="center">PSNR</td>
    <td align="center">SSIM</td>
    <td align="center">PSNR</td>
    <td align="center">SSIM</td>
  <td align="center"><a href="https://mega.nz/folder/Ph0DyJJL#XTYf0aa0_sQ61-Y4LiiFmQ">Link</a></td>    
  </tr>
</thead>
<tbody>
  <tr>
    <td align="center"></td>
    <td align="center">38.68</td>
    <td align="center">0.981</td>
    <td align="center">29.13</td>
    <td align="center">0.868</td>
    <!-- <td align="center"><a href="https://mega.nz/folder/Ph0DyJJL#XTYf0aa0_sQ61-Y4LiiFmQ">Link</a></td> -->
  </tr>
</tbody>
</table>

<br>

## Results

CNN U-Net:
The image shows the rainy input image (left), the model output (middle), and the ground truth image (right). The image restoration was quite successful, with a PSNR of 31.13.

<img width="593" alt="Screenshot 2024-05-26 at 6 00 52 PM" src="https://github.com/slakhiani/Rainy-Image-Restoration/assets/135447183/4ba0ab02-fa08-4287-8d74-6e927af75d8e">

