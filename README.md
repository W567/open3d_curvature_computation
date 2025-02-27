# Open3D -- Estimating Discrete Total Curvature with Per Triangle Normal Variation

A universal total curvature estimation method that works for both triangle meshes and point clouds. For details, see the [SIGGRAPH 2023 paper](https://arxiv.org/abs/2305.12653) by Crane Chen under the supervision of Misha Kazhdan.

This codebase was developed on MacOS 12.6, adapting from the template code of open3d, [open3d-cmake-find-package](https://github.com/isl-org/open3d-cmake-find-package.git), original research code can be found [here](https://github.com/HeCraneChen/total-curvature-estimation.git).
<img width="809" alt="o3d_curvature_teaser" src="https://github.com/HeCraneChen/open3d-discrete-total-curvature/assets/33951209/3297f9f8-9811-42de-8650-41397a10d3cc">

## Comparison with other popular libraries
![teaser_bright](https://user-images.githubusercontent.com/33951209/229387054-371fa8e9-1ef2-4552-81e3-af6927ee99dc.png)

## Dependencies

- [open3d](https://github.com/isl-org/Open3D.git)
- [STL](https://www.geeksforgeeks.org/the-c-standard-template-library-stl/)
- [eigen](https://eigen.tuxfamily.org/index.php?title=Main_Page) for matrix data structures
- [openmp](http://polyscope.run/) for parallelization
- [cgal](https://www.cgal.org/) for delaunay triangulation


## Run

On MacOS, just issue (make sure that Open3D and CGAL are already installed on your machine, use Homebrew to install CGAL on MacOS):

    git clone https://github.com/HeCraneChen/open3d-discrete-total-curvature.git --recursive
    cd open3d-discrete-total-curvature
    cd build
    ./Draw
    

![o3d_curvature_output](https://github.com/HeCraneChen/open3d-discrete-total-curvature/assets/33951209/81265c20-8aa2-454f-aa6f-52f2c68af776)


**Compile**

Compile this project from scratch using the standard cmake routine (make sure that Open3D and CGAL are already installed on your machine, use Homebrew to install CGAL on MacOS):

    cd open3d-discrete-total-curvature
    rm -r build
    mkdir build
    cd build
    cmake ..
    make
    # to install curvature_computation as a python package
    sudo make install

## Citation

```bibtex
@inproceedings{10.1145/3587421.3595439,
author = {Chen, Crane He},
title = {Estimating Discrete Total Curvature with Per Triangle Normal Variation},
year = {2023},
isbn = {9798400701436},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3587421.3595439},
doi = {10.1145/3587421.3595439},
booktitle = {ACM SIGGRAPH 2023 Talks},
articleno = {56},
numpages = {2},
location = {Los Angeles, CA, USA},
series = {SIGGRAPH '23}
}
```

