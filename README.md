# Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres

## Effect of using `kappa` scheduler. Comparative analysis of using the `kappa` scheduler on two datasets for various evaluation metrics.
<table>
  <tr>
    <th></th>
    <th colspan="2">CIFAR10</th>
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

## Comparative analysis of `Euclidean` and `Angular` based reverse denoising step for `CIFAR-10` dataset. Various score functions are also used for evaluation.
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

## Comparative analysis of `Euclidean` and `Angular` based reverse denoising step for `MNIST` dataset.
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

## Comparative analysis of `Euclidean` and `Angular` based reverse denoising step for `D-LORD` dataset
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


## Sample Distribution across Sub-Cones (Gaussian vs. vMF)
![collage_page-0001](https://github.com/aryachiranjeev/Harmonizing-Geometry-and-Uncertainty-Diffusion-with-Hyperspheres/blob/main/sample_distribution_subcone.png)

### Quantitative Metrics
#### Gaussian-based
	Mean Cosine Similarity = 0.900
	Std Dev = 0.048 (Low variance, meaning samples are mostly near the mean)
#### vMF-based
	Mean Cosine Similarity = 0.722
	Std Dev = 0.137 (Higher variance, meaning samples are spread across different difficulty levels)
 
