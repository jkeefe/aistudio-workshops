# AI Studio Workshops

This code supports workshops taught by members of the Quartz AI Studio for getting journalists learning machine learning.

## A note about notebooks

These workshops exist in Jupyter Notebooks (formerly IPython notebooks, which is why notebook files end in `.ipynb`). Because we'll be doing machine learning, we also need a GPU, which is a fast parallel-processor that speeds up the math we use for training models. 

At the time of this writing, the [Google Colaboratory](https://colab.research.google.com) platform provides both a notebook enviroment _and_ a GPU for free. So these notebooks are designed to work particularly well with Google Colab.

If you know how to spin up another platform – such as Amazon's EC2 – the notebooks should work there, too.

## Getting started, with Google Colab

Here's how to get started with these workshops uing Google Colaboatory.

- Go to [Google Colaboratory](https://colab.research.google.com).
- In the top bar of the welcome window, pick "Github."
- Enter `quartz/aistudio-workshops` on the long blue line and press Return.
![Choose "Github"](images/pick_github.jpg)
- From the list that appears, pick the notebook for the lesson you'd like.
![Pick the notebook matching the lesson](images/pick_notebook.jpg)
- You want to run the first code cell in the notebook, by tapping the "play" button on the cell that includes the code `## ALL GOOGLE COLAB USERS RUN THIS CELL`
![Play the first code cell of the notebook](images/play_first_cell.jpg)
- You will get a couple of fun warnings:
![Click through the first warning](images/non_google_warning.jpg)
![Click through the second warning](images/reset_runtimes.jpg)
- Now we need to turn on the GPU! From the "Runtime" menu, pick "Change runtime type."
![Pick change runtime type](images/change_runtime.jpg)

- Then form the "Hardware accellerator" dropdown, pick "GPU."

<img src = "./images/pick_gpu.jpg" alt="Pick GPU" width=300 style="border:2px solid black"> 


