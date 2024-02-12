I'm ready to try using transformers to classify the HuffingtonPost new data, and will install a separate environment for the Huggingface transformers library and its dependent packages.

1. In Anaconda Navigator, created new environment, based on Python 3.8.16
2. Added transformers --  it has also installed numerous other dependent libraries. 
3. Added pytorch, with its dependencies.
4. Added accelerate package (will need this for HuggingFace's Trainer class)
5. Added ipykernel package (needed to run transformers package in jupyter notebook)
6. For completeness of the ML environment, added scikit-learn, imbalanced-learn, matplotlib, and seaborn

When I tried to import the packages in the DistilBERT notebook, was prompted with: 
`TqdmWarning: IProgress not found. Please update jupyter and ipywidgets. See [https://ipywidgets.readthedocs.io/en/stable/user_install.html](https://ipywidgets.readthedocs.io/en/stable/user_install.html) from .autonotebook import tqdm as notebook_tqdm`

Rectified according to the advice here: https://stackoverflow.com/questions/75349025/vs-code-jupyter-notebook-iprogress-not-found

1. Install ipywidgets (in Anaconda Navigator, like for other packages above). All other dependencies, such as widgetsnmextension and iprogress, will be installed alongside as well.
2. Restart VSCode and the notebook should run without complaint to import all the packages. 
