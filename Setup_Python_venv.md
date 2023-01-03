1. create folder for venv
2. create venv
    python -m venv projectname
3. activate it 
    .\Scripts\activate
4. Now, from inside the environment install ipykernel using pip:
    pip install ipykernel
5. And now install a new kernel:
    ipython kernel install --user --name=projectname
At this point, you can start jupyter, create a new notebook and select the kernel that lives inside your environment.
