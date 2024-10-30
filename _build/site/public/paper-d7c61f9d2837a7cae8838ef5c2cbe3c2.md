---
numbering:
  heading_2: false
  figure:
    template: Fig. %s
---

+++ { "part": "abstract" }
In the evolving landscape of scientific research, the ability for papers to "talk to each other" represents a transformative shift towards next-generation literature. This concept, exemplified by the meta-analysis conducted in this Jupyter Notebook, underscores the profound impact of interconnected research facilitated by advanced tools like NeuroLibre, the myst content server, and mdast.
+++


## Case Study

<img src="https://github.com/neurolibre/brand/blob/main/png/neuroxlink.png?raw=true" style="height:60px;"></img>

NeuroxLink is a mini python package to parse [mdast](https://github.com/syntax-tree/mdast), facilitating cross-paper import of article content from MyST servers. It also introduces some [Plotly](https://plotly.com) functionality to work with data from interactive figures! 

:::{figure} #fig1cell
:label: fig1

Doing it live... Importing the mriscope review article!
:::

Let's access some data from the mriscope review article!

:::{figure} #fig2cell
:label: fig2

Structured data extracted from the front-matter of the article.
:::

Maybe there are some interactive figures in this article? Let's inspect the content of the article to find out!

:::{figure} #fig3inspect
:label: fig3

Inspecting the content of the article to find interactive figures using nlx.
:::

Cool! It seems there is an interactive figure in this article. Let's fetch it using nlx, create a plotly object from the structured data and display it!

:::{figure} #fig3cell
:label: fig31

Fetching the interactive figure and displaying it using Plotly.
:::


Note that **we are not performing any computation here**, instead, **we are taking a special chunk of the paper we imported as structured data and creating a plotly figure out of it**!

:::{tip}
We can treat Plotly as our data standard for interactive figures. Behind the scenes, neuroxlink is parsing these plotly objects to return as the part we are interested in!
:::


:::{figure} #fig4cell
:label: fig4

Pandas dataframe created from the structured data of the interactive figure.
:::


<hr>

<img src="https://github.com/agahkarakuzu/alienpaper1/blob/main/static/banner.jpg?raw=true"></src>

## Now we are talking! Or, is it papers talking to each other? 

`#TalkAboutInsight`



Let's start our meta-analysis by importing 15 figures from 5 ALBERTA studies into this article!

:::{figure} #fig5cell
:label: fig5

A mosaic plot of the 15 figures imported into this article from 5 ALBERTA studies.
:::

### Correlation matrix

Remember that 5 studies are seeking to understand the relationship between different brain measurements across different brain regions associated with different cognitive functions. However, despite the simplistic nature of the overall methodology, nearly each article represented the bivariate relationship between two variables using a different method!

If this was a traditional paper, we would not be able to run any meta-analysis on these results, since we cannot combine the data across these studies with the reported methods. 

God news is, this is not a traditional paper! We are in a realm where papers can talk to each other, and we can leverage this power to run a meta-analysis on these results!

:::{figure} #fig6cell
:label: fig6

Scatter plot matrix of the 15 figures imported into this article from 5 ALBERTA studies.
:::

### If you are not convinced that the alines are sooo linear in the brain, check out this PCA plot!

:::{figure} #fig7cell
:label: fig7

PCA plot of the correlations to see the main components that explain the variability in the data.
:::

and this looks almost exactly like the correlation between the `score` and `volume`:

:::{figure} #fig8cell
:label: fig8

Scatter plot of the correlations between the `score` and `volume`.
:::


### Take home message: Hang out with the aliens with bigger heads!

If you were wondering whether the type of correlation method used in each study affects the results of the meta-analysis, here's your meta-meta-analysis:

:::{figure} #fig9cell
:label: fig9

Correlation matrix that you can toggle across different correlation methods.
:::


#### Enhanced Collaboration and Integration

Traditionally, scientific papers have existed in silos, each presenting its findings in isolation. However, the integration of interactive figures and data across multiple papers, as enabled by NeuroLibre, allows for a seamless flow of information. This interconnectedness fosters enhanced collaboration among researchers, enabling them to build upon each other's work more effectively. By remixing data from interactive figures, researchers can combine insights from various studies, leading to more comprehensive and robust conclusions.

#### Accelerated Discovery and Innovation

The ability for papers to communicate and share data accelerates the pace of discovery. Researchers no longer need to manually extract and reanalyze data from individual studies. Instead, tools like the myst content server and mdast facilitate the automatic import and parsing of data, streamlining the research process. This efficiency not only saves time but also reduces the likelihood of errors, allowing researchers to focus on innovative analysis and interpretation.

#### Democratization of Data

Interconnected papers democratize access to data, making it easier for researchers from diverse backgrounds and institutions to contribute to and benefit from collective knowledge. This inclusivity is crucial for addressing complex, multidisciplinary challenges that require diverse perspectives and expertise. By enabling data remixing and integration, platforms like NeuroLibre ensure that valuable insights are not confined to a single study but are accessible to the broader scientific community.

#### Comprehensive Meta-Analyses

Meta-analyses, such as the one demonstrated in this notebook, are significantly enhanced by the ability to integrate data from multiple sources. The NeuroLibre platform's capability to remix data from interactive figures across different papers allows for a more thorough and nuanced analysis. This comprehensive approach leads to more accurate and generalizable findings, ultimately advancing the field and informing future research directions.

#### Conclusion

The concept of "papers talking to each other" is not just a futuristic vision but a present reality enabled by cutting-edge tools and platforms. By facilitating the integration and remixing of data from multiple studies, NeuroLibre, the myst content server, and mdast are paving the way for next-generation scientific literature. This interconnected approach enhances collaboration, accelerates discovery, democratizes data access, and enables comprehensive meta-analyses, ultimately driving the advancement of knowledge and innovation in the scientific community.

#### Introduction and Setup

The notebook begins with an introduction to the ALBERTA studies and the NeuroxLink package, which facilitates cross-paper import of article content and interactive figures.

* Package Installation and Initialization

NeuroxLink is installed and initialized to import and parse data from the specified articles.

* Data Import and Inspection

The notebook imports data from five ALBERTA articles and inspects the available Plotly figures within these articles.

* Data Extraction and Visualization

  - Interactive figures are fetched and rendered using Plotly.
  - Data from these figures is extracted and stored in a structured format.

* Meta-Analysis

  A meta-analysis is performed by combining data from multiple figures across the five articles. The combined data is visualized using various Plotly visualizations, including scatter plots and scatter matrix plots.

* Principal Component Analysis (PCA)

PCA is conducted on the combined dataset to reduce dimensionality and visualize the principal components.

* Correlation Analysis

Correlation matrices (Pearson, Kendall, Spearman) are computed and visualized using heatmaps to understand the relationships between different variables.

* Insights and Conclusions

The notebook concludes with insights derived from the visualizations and analyses, highlighting the variability and relationships between different brain measurements across the studies.

Overall, this notebook showcases the integration of multiple research articles, extraction of interactive data, and comprehensive analysis to derive meaningful insights from the combined dataset.