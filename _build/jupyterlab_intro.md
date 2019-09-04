---
redirect_from:
  - "jupyterlab-intro"
interact_link: content/jupyterlab_intro.ipynb
kernel_name: python3
has_widgets: false
title: 'JupyterLab as a framework for Open Science by Default'
prev_page:
  url: /introduction.html
  title: 'Introduction'
next_page:
  url: /write.html
  title: 'Publication ready scientific reports and presentations with Jupyter ecosystem'
layout: episode



title: "JupyterLab as a framework for Open Science by Default"



teaching: 20



exercises: 25



questions:

  - "How can we use JupyterLab for Open Science by default?"

  - "What are JupyterLab extensions?"

  - "How can we extend JupyterLab?"

objectives:

  - "Learn to use JupyterLab for Open Science"

  - "Learn where to find JupyterLab extension"

  - "Learn how to create new JupyterLab extension"

keypoints:

  - "JupyterLab as a tool for all phases of research process."

comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---




 1 - Introduction to JupyterLab


## What is Jupyterlab?

[JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html) is the next-generation web-based user interface for [Project Jupyter](https://jupyter.org/). It is made of modular building blocks:

- File explorer
- Text editor
- Diagram generator
- jupyter notebooks supporting more than 50 different Jupyter kernels
- Terminals
- Outputs

with an easy integration with Jupyterlab extension such as [jupyterlab-latex](https://github.com/jupyterlab/jupyterlab-latex) for live-editing of LaTeX documents, [jupyterlab-git](https://github.com/jupyterlab/jupyterlab-git) and [jupyterlab-nbdime](https://nbdime.readthedocs.io/en/latest/extensions.html) for git integration, [jupyterlab-drawio](https://github.com/QuantStack/jupyterlab-drawio) for creating diagrams and [jupyterlab-zenodo](https://pypi.org/project/jupyterlab-zenodo/) to easily publish research work and get proper [DOI](https://www.doi.org/).

![JupyterLab ecosystem](images/jupyter_ecosystem.png)

See [JupyterLab slides](https://github.com/jupyterlab/jupyterlab-demo/blob/master/slides/jupyterlab-slides.pdf) from [JupyterLab Github demo repository](https://github.com/jupyterlab/jupyterlab-demo) for more information about JupyterLab. 




## Create a new isolated environment

Whenever you start with a new research project, it is good practice to create a new **isolated** environment, for instance:

-  **[conda](https://docs.conda.io/en/latest/)** to record all the dependencies, with well defined versions
- **[docker](https://www.docker.com/)** or **[Singularity](https://sylabs.io/docs/)** containers to bundle all the necessary ingredients (data, code, environment).

For this short workshop, we have prepared a [github repository](https://github.com/coderefinery/osip) to be run with [mybinder](https://mybinder.org/):

- Click [here](https://mybinder.org/v2/gh/annefou/jupyter_publish_osip/master?urlpath=lab) or on the **Interact** button at the top of this page to start the workshop.

[![Interact button](images/interact_button.png)](https://mybinder.org/v2/gh/coderefinery/osip/master?urlpath=lab)



## Get familiar with Jupyterlab


Start JupyterLab:

![JupyterLab interface](images/jupyterlab.png)

You can also run the [JupyterLab demo](https://github.com/jupyterlab/jupyterlab-demo) with [Binder](https://mybinder.org/v2/gh/jupyterlab/jupyterlab-demo/master?urlpath=lab/tree/demo/Lorenz.ipynb).



## JupyterLab extensions

The JupyterLab Graphical User Interface varies depending on the available kernels (`python`, `R`, `julia`, etc.) but also on the [JupyterLab extensions](https://jupyterlab.readthedocs.io/en/stable/user/extensions.html) you have installed.
And this is where JupyterLab differs from the "classical" Jupyter Notebooks.

> ## Warning
> JupyterLab extensions make JupyterLab highly flexible and can really offer a fully customized user environment but 
> the following recommendations are **important**:
> - only install extensions you can trust (as it allows to execute arbitrary code on the server, kernel, and in the client’s browser)
> - some extensions may not be compatible with some versions of JupyterLab and may break it (as extensions are developed independently of JupyterLab).
>
{: .callout}


Several extensions have been installed for you to try:

- [jupyterlab-latex](https://github.com/jupyterlab/jupyterlab-latex) for live-editing of LaTeX documents, 
- [jupyterlab-git](https://github.com/jupyterlab/jupyterlab-git) and [jupyterlab-nbdime](https://nbdime.readthedocs.io/en/latest/extensions.html) for git integration.


In new version of JupyterLab, an [extension Manager](https://jupyterlab.readthedocs.io/en/stable/user/extensions.html) has been included to facilitate the management of extensions in JupyterLab. 

> ## Remark
> When using JupyterLab through binder
> - installation of additional extensions is usually not possible.
> - [configuration of git](https://swcarpentry.github.io/git-novice/02-setup/index.html) (and github for accessing remote repositories) needs to be done.
> 
{: .callout}




Finally, as you probably already guessed, JupyterLab extensions can be developed independently of JupyterLab itself and anyone can create and distribute new extensions. You can find a step by step tutorial on [how to create a new extension](https://jupyterlab.readthedocs.io/en/stable/developer/extension_tutorial.html). However, before starting any new development, make sure you find out whether this extension already exist or not.

