# Project Proposal

 
### **Client:** <br>

The client is [Latitude](https://latitude.io/#top). They are an emerging gaming company. They specialize in AI generated content. Their initial release [AI Dungeon](https://play.aidungeon.io/main/home) is a text based roleplay adventure game using language models to generate content. <br>

***

### **Question/Need:**<br>


The company would like to improve their user experience. We would like to provide insights on how people interact using natural language within these roleplay scenarios. 
<br>

The goal of this project is to find more generalized underlying interactions in table top roleplay.
<br>

***

### **Data Description:**<br>

The data used will be transcripts of table top roleplay sessions. Specifically, we will use [transcripts](https://huggingface.co/datasets/crd3) of [Critical Role](https://criticalrole.fandom.com/wiki/Critical_Role_Wiki) (a popular DnD group). We are prepared to supplement our data with transcripts from other DnD and roleplay content creators such as [Dimension 20](https://dimension20.fandom.com/wiki/Dimension_20_Wiki).<br>
***

### **Solution Path:**<br>

- **Data** 
  - There is a publicly available dataset with Critical Role [transcripts](https://huggingface.co/datasets/crd3).
  - There is the possibility to double/triple the data by using webscraping to gather more transcripts

- **Preprocessing**
  - Transcripts will need to be trimmed to remove irrelvant sections
    - If these sections are not labeled, we can most likely remove the beginning and tailing sections of text.
  - Transcripts will then be seperated to individual exchanges
    - An individual exchange (uninterupted speech from one person) will represent one document
    - After, splitting transcripts we can expect >100,000 documents in our corpus
  
  - *Cleaning & Engineering*
    - We will need to explore various levels of text cleaning and preprocessing to find the optimal levels for our use case 
- **Modeling**
  - Topic modelling
    - LDA
    - PCA
- **Additional analyses**
  - Explore topics by role of speaker (DM vs Player)
  - Utilze generated topics to augment text generation 
<br>

***

### **Criteria for Success:**<br>

Topics generated make intuitive sense when examined with content expertise. 
<br>

***

### **Assumptions and Risks:**<br>

Topics generated will align with the kind of interactions and not general content within different sessions.
<br>
***

### **Tools:**<br>
Sklearn will be used for modeling. 

Plotly will be used for visualization.

Spacy/NLTK will be used for text processing. 

Huggingface/TF may be used for fine tuning a text generation model

Gradio may be used for creating a demo 
<br>

***

### **Communication:**<br>
A slide presentation will be made explaining insights from analyses

A demo web app will be presented allowing for live demonstration/exploration 

<br>

***

### **MVP Goal:**<br>

An MVP for this project will consist of a list of naive topics generated with minimal tuning