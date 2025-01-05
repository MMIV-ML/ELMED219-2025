# Lab 1: Network science and Patient Similarity Networks (PSN)

This lab will give a quick example-based introduction to basic ideas in **graph theory**, **network science**, and the concept of **patient similarity networks** (PSN) using *NetworkX* - a Python package for the creation, manipulation, and study of the structure, dynamics, and functions of complex networks.


<img src="../assets/GPT-MedAI.png" width="500"><br>

If you have a subscription to [ChatGPT Plus](https://openai.com/blog/chatgpt-plus), you can also try out the the [**Medical AI Assistant (UiBmed - ELMED219 & BMED365)**](https://chat.openai.com/g/g-d90dfN17H-medical-ai-assistant-uibmed-elmed219-bmed365) and see if you can get it to answer some of your questions related to graph theory, network science and patient similarity network, cfr.[[here](./assets/ELMED219_BMED365_2024_PSN.pdf)].

- _Hva er grafteori og hvordan defineres en graf? (answer in English, please)_
- _Hva menes med "nettverk-vitenskap"?_
- _Hva karakteriserer et "patient similarity network" og hva kan det brukes til?_

( compare the responses to the prompts above using the UiB-internal **https://chat.uib.no** )

### Slides


<a href="https://docs.google.com/presentation/d/e/2PACX-1vRvl54T7fBoOQaKCHOUcDDxuB4jDWyjw5tQMv3x5LYL7XVfB2hKGJZar1k3jrEUupYmQYOaMqyJ6MmF/pub?start=false&loop=false&delayms=3000"><img src="assets/Lab1-slide0.png"></a>



### Notebooks



| Notebook    |      1-Click Notebook     
|:----------|------|
|  [00-introduction-slides.ipynb](https://nbviewer.org/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/notebooks/00-introduction-slides.ipynb)  <br>A short introduction to Graph theory, Network science and Patient similarity networks for medical students - an AI-assisted notebook prompted and created in "15 minutes" with [cursor](https://www.cursor.com) and [claude-3.5-sonnet](https://www.anthropic.com/news/claude-3-5-sonnet). | [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/notebooks/00-introduction-slides.ipynb)<br>
|  [01-networkx-tutorial.ipynb](https://nbviewer.org/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/notebooks/01-networkx-tutorial.ipynb)  <br>You can use NetworkX to construct and draw graphs that are undirected or directed, with weighted or unweighted edges. A large collection of functions to analyze graphs is available. This tutorial takes you through a few basic examples and exercises | [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/notebooks/01-networkx-tutorial.ipynb)<br>
|  [02-patient-similarity-networks-iris.ipynb](https://nbviewer.org/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/notebooks/02-patient-similarity-networks-iris.ipynb)  <br>Rather than patient-derived data, we are using the famous  IRIS flower dataset with 4 different measurements from each of the 150 flowers - construction and exploring the "IRIS Flower Similarity Network" | [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/notebooks/02-patient-similarity-networks-iris.ipynb)<br>
|  [03-patient-similarity-networks-ibs-brain.ipynb](./notebooks/03-patient-similarity-networks-ibs-brain.ipynb)  <br>Patient Similarity Networks using data from the paper _Brain morphometry and cognitive features in prediction of irritable bowel syndrome_ [[preprint](https://www.preprints.org/manuscript/202412.2149/v1)] (https://github.com/arvidl/ibs-brain)| [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/notebooks/03-patient-similarity-networks-ibs-brain.ipynb)<br>

</p>

#### See also the [GraphTheory-and-ComplexNetworks](./GraphTheory-and-ComplexNetworks/README.md) notebooks:
- [1-Introduction.ipynb](./GraphTheory-and-ComplexNetworks/notebooks/1-Introduction.ipynb) [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/GraphTheory-and-ComplexNetworks/notebooks/1-Introduction.ipynb) 
- [2-Fundamentals.ipynb](./GraphTheory-and-ComplexNetworks/notebooks/2-Fundamentals.ipynb) [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/GraphTheory-and-ComplexNetworks/notebooks/2-Fundamentals.ipynb)
- [3-Extensions.ipynb](./GraphTheory-and-ComplexNetworks/notebooks/3-Extensions.ipynb) [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/GraphTheory-and-ComplexNetworks/notebooks/3-Extensions.ipynb)
- [4-Network-topology.ipynb](./GraphTheory-and-ComplexNetworks/notebooks/4-Network-topology.ipynb) [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/GraphTheory-and-ComplexNetworks/notebooks/4-Network-topology.ipynb)
- [5-Network-analysis-centrality.ipynb](./GraphTheory-and-ComplexNetworks/notebooks/5-Network-analysis-centrality.ipynb) [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/GraphTheory-and-ComplexNetworks/notebooks/5-Network-analysis-centrality.ipynb)
- [6-Network-analysis-across-time.ipynb](./GraphTheory-and-ComplexNetworks/notebooks/6-Network-analysis-across-time.ipynb) [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MMIV-ML/ELMED219-2025/blob/main/Lab1-NetworkSci-PSN/GraphTheory-and-ComplexNetworks/notebooks/6-Network-analysis-across-time.ipynb)






## Other resources on Graphs and Networks
A. Lundervold \& the Medical AI Assistant: _Elements of graph theory and patient similarity networks (PSN) - A short introduction for ELMED219+BMED365_ [[PDF](./assets/ELMED219_BMED365_2024_PSN.pdf)] [[$\LaTeX$](https://www.overleaf.com/read/pccnktqbnswg#4f47e2)]

For medical and biomedical students new to graph theory, the following online tutorials and resources provide a gentle introduction:

- **Khan Academy Introduction to Graph Theory:** A beginner-friendly series covering basic concepts and applications. [Khan Academy Graph Theory](https://www.khanacademy.org/computing/computer-science/algorithms/graph-representation/a/describing-graphs)
    
- **Graph Theory Tutorials by Sarada Herke:** A YouTube playlist offering visual and intuitive explanations of graph theory concepts. [Sarada Herke's Graph Theory Tutorials](https://www.youtube.com/playlist?list=PLoJC20gNfC2gmT_5WgwYwGMvgCjYVsIQg)
    
- **Introduction to Graph Theory for Medical Students:** [Notes](https://docs.google.com/document/d/1Hy68-fjs1EJV3LL03qYusYydyXP7IAwsUnIYlaC9MdE/edit?usp=sharing) generated by Gemini Advanced 1.5 Pro with [Deep Research](https://blog.google/products/gemini/google-gemini-deep-research)

As Jupyter Notebook is quite new to many of you, you may want to skim through some tutorials. Here are two: 
* https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/index.html
* https://www.datacamp.com/community/tutorials/tutorial-jupyter-notebook
<!-- Here's a short extra video that goes through a very similar notebook to the one we use in this lab: https://www.youtube.com/watch?v=OhxUgFNnj1U. You may want to watch this as well. -->

<hr>

### Your turn! 

Spend some time playing around with the provided examples. You'll find some questions for you to investigate in the notebooks. If you're already familiar with graphs and networks, you can try your hand at more advanced examples or, even better, help out other less experienced team members. 
