# PACE - Applications of Machine Learning

Once connected to the VPN, log in to ondemand-pace-ice.pace.gatech.edu using your GT credentials and submit an interactive Jupyter job to the PACE-ICE default queue.

### Environment Preparation (PACE-ICE Cluster)
1. Once an Jupyter job has started, oprun the following commands to prepare an environment:
  - `conda create --prefix ~/PACEMLenv python=3.10 ipykernel`
  - `conda activate ~/PACEML`
  - `pip install intel-tensorflow-avx512==2.9.1 matplotlib pandas seaborn scikit-learn`
2. Clone this repo to your home directory and change directory:
  - `git clone https://github.com/dphanish/PACE-Apps-of-ML.git`
3. From the main notebook dashboard, launch "PACE-Apps-of-ML/PACE-App_of_ML.ipynb"

If there not enough space in home folder, you could alternatively create the environment in the temporary Scratch running the below commands before conda create (no prefix): 

- `mkdir ${TMPDIR}/.conda`
- `ln -s ${TMPDIR}/.conda ${HOME}/.conda`

For running with GPU, install `tensorflow-gpu` package and launch the ondemand session with `Anaconda3 - Tensorflow GPU` module and `PACE ICE GPU` queue.

*If you want to save your environment, you can run commands like `conda env export` or `conda env export --from-history` or `pip freeze`*
