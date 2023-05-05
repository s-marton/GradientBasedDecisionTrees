This code is used to generate the results for the paper "Learning Decision Trees with Gradient Descent". The required versions of all packages are listed in the dependencies file and can be installed running "install_requirements.sh".

We further provide the following files to reproduce the results from the paper:
    - GDTs-BINARY-HPO: Load the optimized parameters and generate results for all binary classification datasets from paper.
    - GDTs-MULTI-HPO: Load the optimized parameters and generate results for all multi-class classification datasets from paper.
    - GDTs-BINARY-DEFAULT: Use defualt parameters for all approaches and generate results for all binary classification datasets from paper.
    - GDTs-MULTI-DEFAULT: Use defualt parameters for all approaches and generate results for all binary classification datasets from paper.
    - GDTs-SINGLE: Standalone notebook for comparing the different approaches on a single trial for a specified dataset. This notebook provides the best overview on how to use our approach (GDTs).

By default, the GPU is used for the calculations of GDT and DNDT. This can be changed in the config ("use_gpu"). If you receive a memory error for GPU computations, this is most likely due to the parallelization of the experiments on a single GPU. Please try to reduce the number of parallel computations ("n_jobs") or run on CPU (set "use_gpu" to "False"). Please note that the single-GPU parallelization reduces the overall runtime of the experiments, but negsatively influences the individual runtimes. Therefore the runtimes noted in the paper are generated in a separate setting without single-GPU parallelization of multiple trials/datasets.

We further want to note that it is unfortunately not possible to generate reproducible results on a GPU with tensorflow. However this only results in minor deviations of the performance and does not influence the results shown in the paper.

The Python version used in the experiments was Python 3.11.3.