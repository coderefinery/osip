---
interact_link: content/C:\Users\annefou\Documents\Github\coderefinery\osip-book\osip\content\write.ipynb
kernel_name: python3
has_widgets: false
title: 'Publication ready scientific reports and presentations with Jupyter ecosystem'
prev_page:
  url: /jupyterlab_intro.html
  title: 'JupyterLab as a framework for Open Science by Default'
next_page:
  url: 
  title: ''
layout: episode



teaching: 20



exercises: 25



questions:

  - "How can generate outputs in different formats?"

  - "What tools can I use?"

objectives:

  - "Learn to about nbconvert, jupyter-book"

keypoints:

  - "Generate different documents from a set of notebooks."

comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---




In this episode, we will learn how to generate different support to document/publish our research results. 

> ## Discussion (5mn)
> This discussion exercise is to be done in small groups (2-3 persons per group):
> - How do you document your research (inline with the code, jupyter notebooks, etc.)?
> - Where do you store your documents?
> - Do you share all your documents?
> - What tools/formats do you use (Word, LaTeX, Markdown, etc.)?
> 
{: .task}

JupyterLab can also be used to write and document your research to keep our research work. Let's have a quick overview of these possibilities.



# Live editing of Markdown documents

![New markdown file](images/jupyterlab-markdown.png)

If you have an old version of JupyterLab, this **Markdown** icon may not be available; Then use the **Text** icon instead and rename your file (for instance *index.md*). Live editing of Mardkown documents is anyway available:

# Find short online guide for mastering markdown

Markdown language is often used to format readme files and these files are "nicely" rendered by [Github](https://github.com/).

## Where can I learn Markdown?

You already know a large part of markdown as the key aspect of the markdown language is that you can write plain text.

If you plan to use Markdown for commenting/publishing your research work on github, an online guide for [mastering markdonw](https://guides.github.com/features/mastering-markdown/)

Let's take an example (copy-paste in your newly markdown file:

~~~bash
## Heading

# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading

## Emphasis

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Strikethrough~~

## Lists

### Unordered

+ Create a list by starting a line with `+`, `-`, or `*`
+ Sub-lists are made by indenting 2 spaces:
  - sub-list-1
    - sub-list-2
~~~

To render it in Jupyterlab, right click and select **"Show Markdown Preview"**. Then the rendered page should appear as shown on the figure below:


![Markdown preview](images/markdown-preview.png)


> ## Create website on Github
> 
> Github gives you the opportunity to host webpages and for getting this functionality you need:
> - Push your markdown files in a Github repository and make sure you name the main file `index.md`
> - Enable Github pages for your repository:
> ![enable github pages](https://pages.github.com/images/source-setting@2x.png)
> 
> More information can be found [here](https://pages.github.com/)
>
{: .callout}


# Equations within Markdown documents

If you need to write equations, you can use [LaTeX mathematics](https://en.wikibooks.org/wiki/LaTeX/Mathematics) notations (work both for markdown files and jupyter notebook markdown cells):

```bash
$x^2 * x^2$
```

Would render: $x^2 * x^2$

- A few other examples taken from [Notebook motivating examples](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Typesetting%20Equations.html):


-  The Lorenz Equations  

  - Source:
  
```bash
\begin{align}
\dot{x} & = \sigma(y-x) \\
\dot{y} & = \rho x - y - xz \\
\dot{z} & = -\beta z + xy
\end{align}
```

  - Display:
  
\begin{align}
\dot{x} & = \sigma(y-x) \\
\dot{y} & = \rho x - y - xz \\
\dot{z} & = -\beta z + xy
\end{align}
 

So if you are using LaTeX for the ease of writing equations, markdown language may be a good solution for you!




# Live editing of LaTeX documents

[LaTeX](https://www.latex-project.org/) is very popular in many scientific community for writing publications.


# JupyterLab extension for live editing of LaTeX documents

To be able to compile LaTeX files, you would need to install a LaTeX compiler (and have commands such as `pdflatex`, `xelatex`) 
on your system to generate LaTeX documents. 
If you don't you can still follow this section by clicking at the top on **Interact** button.

> ## Installation of LaTeX on Windows
> On Windows, we recommend the usage of [MikTeX](https://miktex.org/); Please note that MikTeX is available as [a conda package](https://anaconda.org/conda-forge/miktex) too.
> In that case, the setting is much easier because all the LaTeX commands will be available from JupyterLab.
> It can also be installed on Linux or Mac-OSX system.
>
{: .callout}

The [JupyterLab LaTeX](https://github.com/jupyterlab/jupyterlab-latex) extension is not available by default and 
needs to be installed. In case, you need to set it up on your laptop, follow instructions given 
[here](https://github.com/jupyterlab/jupyterlab-latex/blob/master/README.md). 

## Create a new LaTeX document

- Create a new empty file

![New text file](images/jupyterlab-textfile.png)

- Rename it to `report_example.tex` (do not forget to change the file extension from `txt` to `tex`

- Then we will create a very simple LaTeX document and check it out with the JupyterLab:

~~~
\documentclass{article}

\begin{document}

\title{A very Simple \LaTeX document}
\date{}
\maketitle


\end{document}
~~~
{: .language-latex}

- Save it and then right click to select "Show LaTeX preview" as shown in the figure below:


![Preview LaTeX](images/jupyterlab-latex_preview.png)

The `pdf` preview of your document will appear on the right hand side of JupyterLab:


![Preview LaTeX](images/jupyterlab-latex_pdf.png)


> ## Update your LaTeX document
>
> Add new sections in your LaTeX document. What happens?
>  
> > ## Solution
> > 
> > The pdf document is automatically updated!
> {: .solution}
{: .challenge}


> ## Add a bibliography (BibTeX)
>
> Create a new bibtex file with at least one reference and reference it in `report_example.tex`
>  
> > ## Solution
> > 
> > In `report_example.bib`:
> >
> > ~~~
> > @article{einstein,
> >     author =       "Albert Einstein",
> >     title =        "{Zur Elektrodynamik bewegter K{\"o}rper}. ({German})
> >         [{On} the electrodynamics of moving bodies]",
> >     journal =      "Annalen der Physik",
> >     volume =       "322",
> >     number =       "10",
> >     pages =        "891--921",
> >     year =         "1905",
> >     DOI =          "http://dx.doi.org/10.1002/andp.19053221004"
> > }
> > ~~~
> > {: .language-bash}
> >
> > And in `report_example.tex`:
> > 
> > ~~~
> > \documentclass{article}
> > 
> > \begin{document}
> > 
> > \title{A very Simple \LaTeX document}
> > \date{}
> > \maketitle
> > 
> > \section{introduction}
> > 
> > This document shows how to use BibTeX references. 
> > 
> > To cite the Einstein journal paper use \cite{einstein}.
> > 
> > \medskip
> >  
> > \bibliographystyle{unsrt}
> > \bibliography{report_example}
> > 
> > \end{document}
> > 
> > ~~~
> > {: .language-bash}
> >
> {: .solution}
> See [https://fr.overleaf.com/learn/latex/Bibliography_management_with_bibtex](https://fr.overleaf.com/learn/latex/Bibliography_management_with_bibtex)
> to get more examples.
{: .challenge}

# Generate LaTeX from our jupyter notebooks

Being able to create LaTeX live documents with JupyterLab is great but we also need to make use of our jupyter notebooks so we can create a reproducible research work, share it and publish it.

Let's go back to our jupyter notebook example and let's create a nice LaTeX document from it.

- Close `report_example.tex` and `report_example.pdf` and open `example.ipynb`.
- Add a new code cell at the end with the following information:

~~~
!nbpublish -f latex_ipypublish_all -pdf example.ipynb
~~~
{: .language-python}
 
 - Execute this cell and check `converted` directory. It should contain a list of files and in particular:
      * _example.tex_
	  * _example.pdf_


`nbpublish` can be called directly from your jupyter notebook or from the jupyterLab Terminal.

## Cell inspector

It is sometimes convenient to inspect and modify metadata of a given cell. For instance, to ignore the cell where nbpublish is run:


~~~
{ 
   "ipub": {
    "ignore": true
  }
}
~~~
{: .language-bash}

Add it in the metadata of the corresponding cell, as shown in the image below:


![jupyterlab cell inspector](../fig/jupyterlab-ipypublish.png)

Do not forget to *commit changes to data*.

There are several options (not only latex_ipypublish_all) to generate and customize what you would like to see in your report. 


Check the [ipypublish documentation](https://ipypublish.readthedocs.io/en/latest/) for more information. Please note that
the `ipypublish` python package is still under development (beta version avaiable only).

> ## Add generated files into your Github repository
> 
> Add the updated example.ipynb, example.pdf, report_example.tex, report_example.bib and report_example.pdf to your Github
> repository `research-bazaar-jupyter-2019` using JupyterLab git extension and/or JupyterLab Git Terminal. 
> 
{: .challenge}

## Additional ipypublish example

In this short tutorial, all the functionalities of ipypublish are not demonstrated. However, feel free to browse the [following example](https://github.com/annefou/ipypublish_example).


# Combine our Jupyter notebooks and LaTeX documents

Now we can combine our jupyter notebook and our LaTeX document to generate a single publication ready scientific report.

A very simple way to combine them is to merge the pdf generated files. Create a new text file and rename it `report_main.tex`:

~~~
\documentclass{report}
\usepackage{pdfpages}
\usepackage{fancyhdr}
\fancyhf{}
\renewcommand{\headrulewidth}{0pt}
\pagestyle{fancy}
\rfoot{\thepage}
\begin{document}
\tableofcontents
\chapter{A chapter}
\section{Introduction}
\includepdf[pages=1-,pagecommand={\thispagestyle{fancy}}]{report_example.pdf}
\includepdf[pages=1-,pagecommand={\thispagestyle{fancy}}]{example.pdf}
 
 
\end{document}
~~~
{: .language-latex}

Then generate the resulting pdf files ("Show LaTeX preview"). 

> ## Add generated files into your Github repository
> 
> As before, add report_main.tex and report_main.pdf to your Github
> repository `research-bazaar-jupyter-2019` using JupyterLab git extension and/or JupyterLab Git Terminal. 
> 
{: .challenge}



# Jupyter book to create online book from Jupyter notebooks and markdown files

## Jupyter book

A solution to build an online book using a collection of Jupyter Notebooks and Markdown files.

```bash
pip install jupyter-book
```



# Presentations

## Markdown as slides

## Exporting notebooks as slides


