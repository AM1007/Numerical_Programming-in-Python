# Topic 2. Matrix Decompositions and Factorizations in Linear Algebra

**Today, you will use Singular Value Decomposition (SVD) for image compression. This approach can be useful in digital signal processing and preparing data for machine learning models.**

This will help you strengthen the following skills:

- Working with matrix representations of images.

- Applying matrix decompositions.

***

## Task (Step by Step)

**1. Prepare a few images:** These can be RGB images or grayscale images, for example, in JPG format.

**2. Display the images in Colab:** Use the `imread` function from the `matplotlib` library.

**3. Determine the size of the image:** Use the `shape` function.

**4. Since SVD can only be applied to 2D data**, you can either apply it to each color channel separately or reshape the image from a 3D matrix to a 2D matrix by flattening each color channel and stacking them horizontally (or vertically).

For example, you can use the `reshape` function to transform the image into a 2D matrix by stacking the color channels horizontally:

```python
height, width, channels = image.shape
flat_image = image.reshape(-1, width * channels)
```

**5. Apply SVD decomposition:** Use the `svd` function from the `numpy` library.

**6. Visualize the first *k* singular values from the *Σ* matrix.** You can use `matplotlib` for this:

```python
plt.plot(np.arange(k), S[:k])
```

**7. If the plot shows a significant drop in the singular values** from the *Σ* matrix, it means we can effectively compress the image without significant loss of accuracy. For example, to compress the image using the first 100 singular values, you can use the Truncated SVD algorithm (via the `TruncatedSVD` function):

```pyhon
svd = TruncatedSVD(n_components= 100 )
truncated_image = svd.fit_transform(flat_image)
```

**8. To measure the information lost during compression**, we can calculate the reconstruction error. We will measure the reconstruction error as the Mean Squared Error (MSE) between the pixel values of the original image and the reconstructed image.

In Scikit-Learn, the reconstructed image can be obtained by calling the `inverse_transform` method of the `TruncatedSVD` transformer:

```python
reconstructed_image = svd.inverse_transform(truncated_image)
```

The reconstruction error can be calculated as:

```python
reconstruction_error = np.mean(np.square(reconstructed_image - flat_image))
reconstruction_error
```

**9. To visualize the reconstructed image**, we first need to reshape it back to its original 3D form and then clip the pixel values to integers in the range [0, 255]:

```python
reconstructed_image = reconstructed_image.reshape(height, width, channels)
reconstructed_image = np.clip(reconstructed_image, 0 , 255 ).astype( 'uint8' )
```

**10. Experiment with different values of** *k* (the number of singular values from the *Σ* matrix) and visualize the results. At what values of *k* does the loss in image quality become noticeable?

***

## Hints

- Use functions from numpy, sklearn, and algorithms from the lecture notes for this topic.

- Refer to the documentation of numpy, sklearn, and matplotlib for additional guidance.