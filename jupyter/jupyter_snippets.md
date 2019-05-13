## Situation

Your data (may be GB, TB, etc.) is in your working cluster/server. You want to access and interactively play with your data at your home computer. You can use `xwin` to open your Jupyter notebook on remote host. However, this kind of connection is quite slow.

To make the connection faster, you can follow below instructions:

First, make sure you install Jupyter notebook in both remote (working station in your office) and local (your home computer)

In remote host, open the terminal, change directory to where you have your notebooks and type:

`jupyter notebook --no-browser --port=8889`

**NOTE:** Leave the above window open

In your local computer, open a terminal then type:

`ssh -N -f -L localhost:8888:localhost:8889 username@your_remote_host_name`

Now open web browser (Google Chrome, Firefox, etc.) and type:

`localhost:8888`

and you will see your notebooks in your given directory from your remote computer/server.