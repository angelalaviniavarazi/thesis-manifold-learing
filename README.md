# Theoretical Foundations of Manifold Learning

Bachelor of Science thesis by **Angela Lavinia Varazi**  
Bocconi University — Mathematical and Computing Sciences for Artificial Intelligence  
Supervisor: **Prof. Alessandro Pigati**  
Academic year: **2024–2025**

This thesis studies the theoretical foundations of manifold learning: Riemannian geometry, the Laplace–Beltrami operator, graph Laplacians, point-wise and spectral convergence, and Laplacian Eigenmaps. The experimental appendix applies Laplacian Eigenmaps to images from the COIL-100 dataset.

## Files

- [Thesis](ManifoldLearning.pdf): the original thesis, including the experimental figures.
- [Jupyter notebook](ManifoldLearning.ipynb): the nine code cells printed in Appendix A, reconstructed from physical PDF pages 56–62.
- [Requirements](requirements.txt): Python packages needed to work with the notebook.

## Methods in the notebook

1. Unweighted k-nearest-neighbor graph.
2. Heat-kernel weighted matrix.
3. Heat-kernel weighted matrix with an epsilon distance threshold.
4. Unweighted matrix with an epsilon distance threshold.

Each method computes three embedding coordinates and displays 3D and 2D projections. The selected object is object 5, with images at five-degree rotation intervals.

## Run locally

Use Python 3. In a terminal opened in this folder, create an environment and install the requirements:

```sh
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m jupyterlab ManifoldLearning.ipynb
```

On Windows, activate the environment using `.venv\Scripts\activate` instead.

Download the processed [COIL-100 dataset from Columbia University](https://www.cs.columbia.edu/CAVE/software/softlib/coil-100.php). Arrange the extracted images to match the original notebook path:

```text
ManifoldLearning.ipynb
coil-100/
    coil-100/
        obj5__0.png
        obj5__5.png
        ...
```

Run the notebook cells from top to bottom. The first cell selects `object_label = 5`; change it to use another object after obtaining its images. The dataset is downloaded separately and is not included in this repository.

## Reconstruction and reproducibility

The code, comments, spelling, parameters, and original cell boundaries have been preserved from the printed appendix. Indentation and visible blank lines were recovered from the PDF layout. The notebook adds introductory documentation and metadata identifying the original cells (In [94] through In [102]). The original source notebook was not embedded in the PDF, so this reconstruction does not claim byte-for-byte identity with that unavailable file.

Execution counts and outputs are cleared; consult the thesis for the original plots. Python syntax and notebook structure were checked, but the experiments were not executed against the dataset during reconstruction. The PDF does not specify package versions, so `requirements.txt` lists dependencies without claiming to recreate the original environment. Existing algorithm choices are preserved without corrections.

## Dataset reference

S. A. Nene, S. K. Nayar, and H. Murase. *Columbia Object Image Library (COIL-100)*. Technical Report CUCS-006-96, February 1996. [Dataset and documentation](https://www.cs.columbia.edu/CAVE/software/softlib/coil-100.php).
