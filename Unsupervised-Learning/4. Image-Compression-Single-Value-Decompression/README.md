# Image Compression with Singular Value Decomposition (SVD)

## What is SVD?

**Singular Value Decomposition (SVD)** is a fundamental concept in **linear algebra** and is widely used in scientific computing, statistics, and machine learning. It is a type of **matrix factorization** technique that decomposes any real or complex matrix "A" into three other matrices:

\[
A = U \Sigma V^T
\]

Where:
- **\( U \)** is an orthogonal matrix containing the left singular vectors.
- **\( \Sigma \)** (Sigma) is a diagonal matrix with **singular values** (real, non-negative numbers) arranged in descending order.
- **\( V^T \)** is the transpose of an orthogonal matrix containing the right singular vectors.

These matrices represent **rotations and scalings**, and together they describe the structure of the original matrix.

---

## Image Compression and SVD

SVD has a powerful application in **image compression** because digital images can be represented as matrices. Each image channel (like red, green, or blue in RGB images) is a matrix of pixel intensity values.

By applying SVD to each of these matrices, we can approximate the original image by keeping only the **most important singular values** and discarding the rest. This results in a **compressed version of the image** that retains most of its important features but takes up **less memory**.

---

## How It Works

1. **Convert the Image to a Matrix**:
   - Grayscale images are single matrices; colored images can be split into three matrices (R, G, B).

2. **Apply SVD**:
   - Decompose the matrix into `U`, `Σ`, and `V^T`.

3. **Keep Top k Singular Values**:
   - Retain only the top `k` singular values and corresponding vectors.
   - This creates a rank-k approximation of the original matrix.

4. **Reconstruct the Image**:
   - Multiply the reduced matrices to get an approximation of the original matrix/image.
   - The higher the value of `k`, the closer the reconstructed image is to the original.

---

## Visual Tradeoff

- **Small `k`**: Drastically reduces image size but can make the image look blurry or lose detail.
- **Large `k`**: Preserves high image quality but results in less compression.
- **Optimal `k`**: A balance between **quality** and **compression**.

---

## Advantages of Using SVD for Compression

- **Efficient Storage**: Reduces memory usage significantly.
- **Retains Key Features**: Even with fewer singular values, main features like edges and patterns are often preserved.
- **Noise Reduction**: Can remove minor noise by ignoring low singular values.

---

## Disadvantages

- **Computationally Expensive**: Calculating full SVD is resource-intensive for large images.
- **Not Real-Time**: Not suitable for live or streaming scenarios unless optimized.
- **Image Quality Tradeoff**: Reducing singular values too aggressively can result in noticeable degradation.