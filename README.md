# PACE - Applications of Machine Learning

Once connected to the VPN, log in to ondemand-pace-ice.pace.gatech.edu using your GT credentials and submit an interactive Jupyter job to the PACE-ICE default queue.

### Environment Preparation (PACE-ICE Cluster)
1. Once an Jupyter job has started, oprun the following commands to prepare an environment on local scratch:
  - `mkdir ${TMPDIR}/.conda`
  - `ln -s ${TMPDIR}/.conda ${HOME}/.conda`
  - `conda create -y -n app-of-ml python=3.10 ipykernel`
  - `conda activate app-of-ml`
  - `pip install --upgrade protobuf==3.20.0`
  - `pip install intel-tensorflow-avx512==2.9.1 matplotlib pandas seaborn scikit-learn`
2. Clone this repo to your home directory and change directory:
  - `git clone https://github.com/apjez/PACE---Applications-of-Machine-Learning.git`
3. From the main notebook dashboard, launch "PACE---Applications-of-Machine-Learning/PACE-App_of_ML.ipynb"


*If you want to save your environment, you can run commands like `conda env export` or `conda env export --from-history` or `pip freeze`*
