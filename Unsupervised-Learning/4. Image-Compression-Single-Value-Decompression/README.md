# Image Compression with Singular Value Decomposition

## What is SVD?
Singular value decomposition (SVD) comes from linear algebra. It is a matrix factorization technique that decomposes any matrix into three other matrices. SVD expresses a matrix as a combination of rotations, scalings, and one other rotation.

## Image Compression and SVD
SVD is used for image compression as it can reduce the file size of the image by reducing the number of values needed to represent an image.

Any image can be represented by a matrix. SVD then decomposes this matrix into three matrices. SVD keeps only the largest/most significant singular values.

The number of these singular values retained determines the visual quality and file size. Retaining fewer values results in a smaller image size but poor image quality and vice versa. Balancing these two will give a good singular values number. 