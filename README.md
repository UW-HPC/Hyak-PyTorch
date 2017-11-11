# Hyak-PyTorch
Example scripts for running PyTorch on Hyak

# Installing PyTorch
First access a build node:

```
srun -p build -c 2 --pty /bin/bash
```

Load the latest Anaconda module:
```
module load anaconda3_4.3.1
```

Create a virtual environment (optionally install additional deeplearning libraries) and activate:
```
conda create -n deeplearning keras tensorflow
source activate deeplearning
```

Download the latest version of PyTorch:
```
conda install pytorch torchvision -c soumith
```

# Submitting to Scheduler
Include the following lines in your Slurm submission script

```
module load anaconda3_4.3.1
source activate deeplearning
python your_job.py
```
