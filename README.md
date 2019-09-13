# AI Studio Workshops

This code supports workshops taught by members of the Quartz AI Studio for getting journalists learning machine learning.

## Resources

Quartz AI Studio: https://qz.ai
fast.ai: https://fast.ai
practical deep learning: https://course.fast.ai/


## A note about notebooks

These workshops exist in Jupyter Notebooks (formerly IPython notebooks, which is why notebook files end in `.ipynb`). Because we'll be doing machine learning, we also need a GPU, which is a fast parallel-processor that speeds up the math we use for training models. 

At the time of this writing, the [Google Colaboratory](https://colab.research.google.com) platform provides both a notebook enviroment _and_ a GPU for free. So these notebooks are designed to work particularly well with Google Colab.

If you know how to spin up another platform – such as Amazon's EC2 – the notebooks should work there, too.

## Getting started, with Google Colab

Here's how to get started with these workshops uing Google Colaboatory.

- Go to [Google Colaboratory](https://colab.research.google.com).
- In the top bar of the welcome window, pick "Github."
- Enter `quartz` on the long blue line and press Return.

<img src = "./images/pick_github2.jpg" alt="Choose Github" width=600> 

- From the list that appears, make sure `aistudio-workshops` is the selected repository and then click on the notebook for the lesson you'd like.

<img src = "./images/pick_notebook_v3.jpg" alt="Pick the notebook matching the lesson" width=600> 

- Now we need to turn on the GPU! From the "Runtime" menu, pick "Change runtime type."

<img src = "./images/change_runtime.jpg" alt="Pick change runtime type" width=400> 

- Then form the "Hardware accellerator" dropdown, pick "GPU."

<img src = "./images/pick_gpu.jpg" alt="Pick GPU" width=400> 

- You want to run the first code cell in the notebook, by tapping the "play" button on the cell that includes the code `## ALL GOOGLE COLAB USERS RUN THIS CELL`

<img src = "./images/play_first_cell.jpg" alt="Play the first code cell of the notebook" width=700> 

- You will get a couple of fun warnings:

<img src = "./images/non_google_warning.jpg" alt="Click through the first warning" width=500> 

<img src = "./images/reset_runtimes.jpg" alt="Click through the second warning" width=500> 




