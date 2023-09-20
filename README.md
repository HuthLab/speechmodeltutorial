# speechmodeltutorial

Originally given as a tutorial at EACL 2014 by Alex Huth.

In this tutorial you will step through a voxel-wise modeling analysis. You will use computational models to extract semantic features from a natural speech stimulus. Then these features will be used to build linear models of fMRI data, and model weights and prediction performance will be visualized.

If you so desire, you can step through this entire tutorial without modifying any code. But there are a few points where you will be able to make simple modifications and then see what effect those modifications have on the results. Additionally, at the end you can re-run the model using phoneme features instead of semantic features.

#### Acknowledgements
This fMRI data used in this tutorial was collected by Alex Huth and Wendy de Heer at the University of California, Berkeley. All work was supervised by professors Jack Gallant and Frederic Theunissen of the UC Berkeley Psychology Department. Please do not redistribute the code or data used here. Visualization is done using [pycortex](http://pycortex.org).

#### Citation
The analysis demonstrated in this tutorial forms the basis of this paper:
[Huth, A. G. et al., "Natural speech reveals the semantic maps that tile human cerebral cortex" (2016) _Nature_.](https://www.nature.com/articles/nature17637)

Installation
------------
1. Download the [data files](https://utexas.box.com/shared/static/4n3lemyec0wlj5rcr80991nxwflsbks9.zip) and unzip in this directory. Should create a directory called `data`.
2. (If not using Anaconda) install dependencies:
`sudo apt-get update`
`sudo apt-get install -y ipython ipython-notebook python-numpy python-scipy python-matplotlib cython python-pip python-pip python-dev python-h5py python-nibabel python-lxml python-shapely python-html5lib mayavi2 python-tables git`

    (If using Conda): `conda install python 'cython=0.29.36' pytables h5py jupyter matplotlib numpy scipy` (NOTE: some packages may be missing from this list)

    (The cython requirement is from this issue: https://github.com/gallantlab/pycortex/issues/490#issuecomment-1644641810 )
  
4. Fetch and install pycortex:
`git clone https://github.com/gallantlab/pycortex.git`
`cd pycortex; python setup.py install`
5. Start a Jupyter notebook server in this directory (if you don't have one):
`jupyter notebook`
