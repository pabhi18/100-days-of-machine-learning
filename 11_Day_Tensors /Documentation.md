# Day 11: Tensors

Tensors are data structures or containers for numbers, similar to arrays or lists. In fact, matrices and vectors are examples of tensors. Tensors can have any number of dimensions, and are often used in machine learning and deep learning algorithms to represent and manipulate data.

## Types of Tensors

### 0D Tensor:
A 0D tensor is a scalar, which is a single number. For example, the temperature of a room at a given moment can be represented as a 0D tensor.

### 1D Tensor:
A 1D tensor is a vector, which is a list of numbers. For example, the GPAs, IQs, or states of different students can be represented as a 1D tensor.

### 2D Tensor:
A 2D tensor is a matrix, which is a table of numbers arranged in rows and columns. For example, the grades of different students in different subjects can be represented as a 2D tensor.

### ND Tensor:
Tensors with more than 2 dimensions are called ND tensors. They can be represented as arrays with multiple indices.


## Rank, Axes, Shape, and Size

### Rank:
The rank of a tensor is the number of dimensions it has. For example, a 1D tensor has rank 1, a 2D tensor has rank 2, and so on.

### Axes:
Each dimension of a tensor is called an axis. For example, a 2D tensor has two axes: the rows and columns.

### Shape:
The shape of a tensor is a tuple that describes how many elements it has along each axis. For example, a 2x3 matrix has shape (2, 3) because it has 2 rows and 3 columns.

### Size:
The size of a tensor is the total number of elements it contains. For example, a 2x3 matrix has size 6 because it contains 6 numbers.


## Examples of Tensors

### 1D Tensor:
we can represent the GPAs of 5 students as a 1D tensor: <br>
gpa = [3.5, 3.8, 2.9, 4.0, 3.6]

### 2D Tensor
We can represent the grades of 5 students in 3 subjects as a 2D tensor: <br>
grades = <br>  [[85, 90, 92],  <br>
          [90, 92, 88], <br>
          [78, 80, 82], <br>
          [95, 96, 97], <br>
          [88, 92, 90]]

### 3D Tensor
We can represent the greetings "Hi Nitesh", "Hi Rahul", and "Hi Ankit" as a 3D tensor using one-hot encoding: <br>
greetings = <br> [[[1, 0, 0],   # Hi Nitesh <br>
             [0, 1, 0], <br>
              [0, 0, 1]], <br>
             [[1, 0, 0],   # Hi Rahul <br>
              [0, 1, 0], <br>
              [0, 0, 1]], <br>
             [[1, 0, 0],   # Hi Ankit <br>
              [0, 1, 0], <br>
              [0, 0, 1]]] <br>
Here, each greeting is represented as a 3D tensor with shape (3, 3, 1), where each element of the tensor is a one-hot encoded vector representing

### 4D Tensor
4D tensors are commonly used in image processing, where each image is represented as a 3D tensor, consisting of height, width, and channel dimensions. For example, a color image of dimensions 256x256 with 3 color channels (RGB) can be represented as a 3D tensor with dimensions (256, 256, 3). Now, if we want to process a batch of 10 such images, we can create a 4D tensor with dimensions (10, 256, 256, 3), where the first dimension represents the number of images in the batch.

### 5D Tensor
5D tensors are commonly used in video processing, where each video can be represented as a sequence of frames, each of which is a 3D tensor as described above. If we have a video of dimensions 128x128 with 3 color channels and 30 frames, we can represent it as a 4D tensor with dimensions (30, 128, 128, 3). Now, if we want to process a batch of 10 such videos, we can create a 5D tensor with dimensions (10, 30, 128, 128, 3), where the first dimension represents the number of videos in the batch.

