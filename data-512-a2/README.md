# Overview

This assignment contains reproducible analyses of data from the Wikipedia Talk corpus, a data repository of comments on Wikipedia. Crowd-workers annotated these comments, in terms of their aggressiveness, toxicity, and personal hostility, to train machine learning models to assist in automated detection and treatment of contentious online discussions. In this assignment, using the "toxicity" and "aggression" subset datasets from the corpus, we investigate possible biases in the data collection and reviewer annotation processes, and discuss all implications with respect to the potential applications thereof. As an example, Google data scientists use this data to develop related software as part of their [Conversation AI project](https://conversationai.github.io). 

# Structure

- `data/`, all relevant data files (in TSV format)
- `figures/`, all generated visualizations
- `hcds-a2-data-bias.ipynb`, the complete notebook for reproducing and viewing results
- `LICENSE`, a standard MIT license for this work

# Data Sources

The datasets we used (as well as the remaining parts of the corpus that we did not use, are available) as [this Figshare link](https://figshare.com/projects/Wikipedia_Talk/16731). Navigating to the "toxicity" and "aggression" datasets and downloading all content is sufficient (as is using the data in this repository), but you can also directly visit these links and download.

- [Toxicity Data](figshare.com/articles/dataset/Wikipedia_Talk_Labels_Toxicity/4563973)
- [Aggression Data](figshare.com/articles/dataset/Wikipedia_Talk_Labels_Aggression/4267550)

__Note:__ if you visit these links and click "Download all", you will notice each download is a zipped folder with multiple elements (i.e., the current contents of `data/`). Extract and relocate these as needed, but make sure you can match them to the files used in our notebook.

# Project References

Wikipedia's "Detox" research project is the core of this assingment; it is the source of the data and additional findings, developments, or products. You may find additional documentation, acknowledgments, or resources about the same at [this link](https://meta.wikimedia.org/wiki/Research:Detox).

Perspective API, a Google-Jigsaw joint venture and tool, is another collaborative research project, that uses this data and subsequent Machine Learning to detect and assist in the moderation of toxic discussions. These links may be helpful:

- [their website](https://www.perspectiveapi.com/#/home)
- [their GitHub wiki page](https://github.com/conversationai/perspectiveapi/wiki/perspective-hacks)
- [their API documentation](https://github.com/conversationai/perspectiveapi/blob/master/2-api/methods.md)


# Dependencies

This notebook runs on a `Python3` environment with the following notable package dependencies:

```
pandas 
seaborn
matplotlib
statsmodels
```