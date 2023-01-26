1. Install mamba via .exe
2. create and activate a virtual mamba environment
    mamba create -n mymambatry
    mamba activate mymambatry
4. Now, from inside the environment install all dependencies:
mamba install -c fastchan fastai ipykernel numpy==1.23.5 pytorch torchvision torchaudio cudatoolkit nbdev duckduckgo_search pytorch-cuda=11.6 -c pytorch -c nvidia
pip install duckduckgo_search
mamba install -c conda-forge ipywidgets

5. And now register a new kernel:
    ipython kernel install --user --name=mymambatry
At this point, you can start jupyter, create a new notebook and select the kernel that lives inside your environment.



Watch the GPU usage:
nvidia-smi --query-gpu=timestamp,pstate,temperature.gpu,utilization.gpu,utilization.memory,memory.total,memory.free,memory.used --format=csv -l 1
