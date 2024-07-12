## Matplotlib 📝


## Programs

- Draw a line in a diagram from position (0,0) to position (6,250)

  ```py
  import matplotlib.pyplot as plt
  import numpy

  x = numpy.array([0, 6])
  y = numpy.array([0, 250])

  plt.plot(x, y)
  plt.show()
  ```
  
  ![download](https://github.com/user-attachments/assets/3dd5d151-bdc9-4916-936d-f5f01dbaa653)


  - The plot() function is used to draw points (markers) in a diagram.
  - By default, the plot() function draws a line from point to point.
  - The function takes parameters for specifying points in the diagram.
  - Parameter 1 is an array containing the points on the x-axis.
  - Parameter 2 is an array containing the points on the y-axis.
  - If we need to plot a line from (1, 3) to (8, 10), we have to pass two arrays [1, 8] and [3, 10] to the plot function.
 
   Draw a line in a diagram from position (1, 3) to position (8, 10):
  ```py
  import matplotlib.pyplot as plt
  import numpy

  x = numpy.array([1, 8])
  y = numpy.array([3, 10])

  plt.plot(x, y)
  plt.show()
  ```

