# Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres

## Table 1: Effect of using `kappa` scheduler. Comparative analysis of using the `kappa` scheduler on two datasets for various evaluation metrics
<table>
  <tr>
    <th></th>
    <th colspan="2">CIFAR-10</th>
    <th colspan="2">MNIST</th>
  </tr>
  <tr>
    <th></th>
    <th>With scheduling</th>
    <th>Without scheduling</th>
    <th>With scheduling</th>
    <th>Without scheduling</th>
  </tr>
  <tr>
    <td><strong>Class-wise Accuracy</strong></td>
    <td>89.35</td>
    <td>72.59</td>
    <td>96.01</td>
    <td>86.48</td>
  </tr>
  <tr>
    <td><strong>FID</strong></td>
    <td>3.52</td>
    <td>6.28</td>
    <td>1.86</td>
    <td>2.11</td>
  </tr>
  <tr>
    <td><strong>HCR</strong></td>
    <td>0.2</td>
    <td>0.37</td>
    <td>0.14</td>
    <td>0.21</td>
  </tr>
  <tr>
    <td><strong>HDS</strong></td>
    <td>0.48</td>
    <td>0.63</td>
    <td>0.52</td>
    <td>0.75</td>
  </tr>
</table>

## Table 2: Comparative analysis of `Euclidean` and `Angular` based reverse denoising step for `CIFAR-10` dataset. Various score functions are also used for evaluation
<table>
  <tr>
    <th></th>
    <th colspan="3">CIFAR-10</th>
  </tr>
  <tr>
    <th></th>
    <th>Euclidean with MSE</th>
    <th>Angular with Cosine</th>
    <th>Angular with Geodesic</th>
  </tr>
  <tr>
    <td><strong>FID</strong></td>
    <td>3.52</td>
    <td>3.28</td>
    <td>3.35</td>
  </tr>
  <tr>
    <td><strong>HCR</strong></td>
    <td>0.2</td>
    <td>0.2</td>
    <td>0.19</td>
  </tr>
  <tr>
    <td><strong>HDS</strong></td>
    <td>0.48</td>
    <td>0.51</td>
    <td>0.47</td>
  </tr>
</table>

## Table 3: Comparative analysis of `Euclidean` and `Angular` based reverse denoising step for `MNIST` dataset
<table>
  <tr>
    <th></th>
    <th colspan="3">MNIST</th>
  </tr>
  <tr>
    <th></th>
    <th>Euclidean with MSE</th>
    <th>Angular with Cosine</th>
    <th>Angular with Geodesic</th>
  </tr>
  <tr>
    <td><strong>FID</strong></td>
    <td>1.86</td>
    <td>1.79</td>
    <td>1.77</td>
  </tr>
  <tr>
    <td><strong>HCR</strong></td>
    <td>0.14</td>
    <td>0.15</td>
    <td>0.14</td>
  </tr>
  <tr>
    <td><strong>HDS</strong></td>
    <td>0.52</td>
    <td>0.47</td>
    <td>0.48</td>
  </tr>
</table>

## Table 4: Comparative analysis of `Euclidean` and `Angular` based reverse denoising step for `D-LORD` dataset
<table>
  <thead>
    <tr>
      <th></th>
      <th colspan="3">D-LORD</th>
    </tr>
    <tr>
      <th></th>
      <th>Euclidean with MSE</th>
      <th>Angular with Cosine</th>
      <th>Angular with Geodesic</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>FID</td>
      <td>9.27</td>
      <td>9.01</td>
      <td>8.97</td>
    </tr>
    <tr>
      <td>HCR</td>
      <td>0.21</td>
      <td>0.19</td>
      <td>0.20</td>
    </tr>
    <tr>
      <td>HDS</td>
      <td>0.62</td>
      <td>0.61</td>
      <td>0.62</td>
    </tr>
  </tbody>
</table>


## Figure 1: Sample Distribution across Sub-Cones (Gaussian vs. vMF)
<img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/sample_distribution_subcone.png" width="400"/>

#### Quantitative Metrics
##### Gaussian-based
	Mean Cosine Similarity = 0.900
	Std Dev = 0.048 (Low variance, meaning samples are mostly near the mean)
##### vMF-based
	Mean Cosine Similarity = 0.722
	Std Dev = 0.137 (Higher variance, meaning samples are spread across different difficulty levels)
 
## Facial Data Synthesis
<img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/facial_data_synthesis.png" width="600"/>


## Figure 2: Visualization of `Training` and `Sampling` process on 2D circles

Training Process             |  Sampling Process
:-------------------------:|:-------------------------:
Gaussian Diffusion: Final Reversed Points            |  vMF Diffusion: Final Reversed Points
<img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/gaussian_final_reversed_points.png" width="400"/> | <img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/vmf_final_reversed_points.png" width="400"/>


Training Process             |  Sampling Process
:-------------------------:|:-------------------------:
Forward Process in vMF-based Diffusion        |  Reverse Process in vMF-based Diffusion 
<img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/gaussian_final_reversed_points.png" width="400"/> | <img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/vmf_final_reversed_points.png" width="400"/>



## Figure 3: 3D Feature representation of the 10-class CIFAR-10 dataset 

Gaussian Diffusion: Reversed            |   vMF Diffusion: Reversed 
:-------------------------:|:-------------------------:
<img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/gaussian_diffusion_reversed_cifar10_3d.png" width="400"/> | <img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/vmf_diffusion_reversed_cifar10_3d.png" width="400"/>

	Feature representation of the 10-class CIFAR-10 dataset generated using Gaussian-based diffusion (left) and vMF-based diffusion (right). 
	The vMF-based sampling aligns generated sample features within class-specific 3D hypercones, while Gaussian-based sampling results in scattered features outside the class-hypercones.


 ## Figure 4: Generated Facial Samples
<img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/fig4a_gaussian_face.png" width="400"/>
<img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/fig4a_vmf_face.png" width="400"/>

	Comparison of samples generated using Gaussian (top row) and vMF diffusion models (bottom row).
 	It highlights the improved variation in pose, illumination, expression, and quality with vMF.


 ## Figure 5: Measuring the variations between `Real` and `Generated` CIFAR-10 samples
 <img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/nearest_neighbor_matching.png" width="400"/>

 	Nearest Neighbor Matching between Generated and Real Samples on CIFAR-10. 
  	Each real sample (blue dot) undergoes a noise addition process, and its denoised counterpart (red cross) is placed in the space. 
   	Dashed lines connect each real sample to its nearest generated counterpart.


 ## Figure 6: t-SNE Visualization of `Real` vs. `Generated` samples
<img src="https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/tsne_10_classes.png" width="400"/>

 	t-SNE visualization of real vs generated samples across 10 classes. 
  	Real samples (dots) and generated samples (crosses) form distinct clusters, demonstrating the model’s ability to capture class-specific structures while introducing some variation in feature representation.

