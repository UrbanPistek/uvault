[Install](https://github.com/google/jax#installation)
[Documentation](https://jax.readthedocs.io/en/latest/notebooks/quickstart.html)
Update conda environment:
```
conda env update --file env.yml
```

Create conda environment:
```
conda env create --file env.yml
```

## Benchmarking and Profiling
To view a trace and some stats, open tensorboard with:
```
tensorboard --logdir /tmp/tensorboard/
```

## JupyterLab
Jupyter Lab is used for initial investigations and visuals. Notebooks used to investigate
image processing techniques and various other algorithms are saved under `notebooks/`.

Install:
```
pip install jupyterlab
```

Start:
```
jupyter lab
```

### Use Conda Environment in Jupyter
Ensure you have `ipykernel` installed:
```
conda install ipykernel
```

Add conda enviroment to jupyter notebooks:
```
python -m ipykernel install --user --name=<environment_name>
```

After this step you should be able to select the conda environment as your python interperter.

## Resources
- https://jax.readthedocs.io/en/latest/notebooks/neural_network_with_tfds_data.html
- https://teddykoker.com/2022/04/learning-to-learn-jax/
- https://github.com/deepmind/optax
- https://optax.readthedocs.io/en/latest/optax-101.html
- https://roberttlange.github.io/posts/2020/03/blog-post-10/