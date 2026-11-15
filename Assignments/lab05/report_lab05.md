# Lab Report — Lab 05: Harris Corner Detector

**Q1. In one phrase, what does `det_coords()` compute?**

**Answer:** Detects corner points in an image.

**Q2. Which library function did you use in Step 2 (`compute_gradients`) to convolve the image with the Sobel kernels?**

**Answer:** `scipy.signal.convolve2d()`

**Q3. In Step 3 (`gradient_products`), what are the three products computed from `Ix` and `Iy`?**

**Answer:** `Ix²`, `Iy²` and `Ix × Iy`.

**Q4. What does Step 4 (`smooth_products`) use to weight each gradient product before summing it over a local window?**

**Answer:** A 2D Gaussian kernel.

**Q5. State the formula used in Step 5 (`det_and_trace`) to compute the determinant from `A`, `B` and `C`.**

**Answer:** `det = (A × B) - C²`

**Q6. State the formula used in Step 6 (`harris_response`) to compute the response `R` from the determinant and trace.**

**Answer:** `R = det - alpha × trace²`

**Q7. What is the default value of `self.alpha` in the constructor?**

**Answer:** `0.05`

**Q8. What is the default value of `self.threshold_val` in the constructor?**

**Answer:** `0.001`

**Q9. Which `skimage` function does Step 8 (`find_peaks`) use to collapse a cluster of high-response pixels down to a single coordinate?**

**Answer:** `skimage.feature.peak_local_max()`

**Q10. In Step 9 (`det_coords`), what coordinate order — `(row, col)` or `(col, row)` — does the returned array use?**

**Answer:** `(row, col)`