# ATLAS.ti

ATLAS.ti is one of many software available to assist with qualitative analysis.
It specially excels in open coding, i.e., attaching interpretations and concepts to the material during the analysis stage.

## Installation

### Web and desktop software

ATLAS.t allows one to use both a desktop software and an online version available via [their website](https://web.atlasti.com/) similar to Google Docs.
At this time, they do not automatically synchronise and you are only able to _export_ a web based project, not import a project into it.

Therefore, you need to choose before doing data analysis if you prefer to work on the web-based version or on the desktop version.

ATLAS.ti Web is perfect for collaborative work: you can conduct annotations on the data together, access code manager and quotations and even create shared memos.
However, ATLAS.ti Web is limited in file formats and analysis tools:
only textual data (`.docx`, `.docx`) and `.pdf` files is supported
and some more advanced features, such as automated detection of names, are not available on the web version.

In this material we use ATLAS.ti web in setting up and coding the project and use ATLAS.ti 23 Desktop version for analysis.
You can follow [desktop only-version](../atlasti_desktop) of this document if you cannot use the web version.

### Licence for the software

You will need a licence to use Atlas.TI.
University of Helsinki provides licence for its students and faculty.
To see this information, choose the right operating system and if you use a computer owned by the university or if its a personal computer:

Affiliation | Operating system | Whose computer | Installation guide
- | - | - | -
University of Helsinki | Mac | University of Helsinki | Install from [Managed Software Center](https://helpdesk.it.helsinki.fi/en/instructions/computer-and-printing/software/installation-universitys-mac-software).
University of Helsinki | Mac | Personal computer | Install from [Download Centre](https://helpdesk.it.helsinki.fi/en/instructions/computer-and-printing/software-download-center/new-download-centre).
University of Helsinki | Windows | University of Helsinki | Install from [Software Center](https://helpdesk.it.helsinki.fi/en/instructions/computer-and-printing/software/software-center).
University of Helsinki | Windows | Personal computer | Install from [Download Centre](https://helpdesk.it.helsinki.fi/en/instructions/computer-and-printing/software-download-center/new-download-centre).

## Starting to use ATLAS.ti

### Setting up the project

After you have logged into [ATLAS.ti Web](https://web.atlasti.com/), you first need to create a new project.
Project contains documents (i.e., what you seek to analyse),
all codes related to those documents,
all memos related to codes and documents
etc.
That is, a project corresponds to a set of materials related to your research project, for example all interview materials for your collection.
Ideally, this corresponds to a cohesive set of materials used in the context of a research project.

<iframe width="560" height="315" src="https://www.youtube.com/embed/KjUhzUqz2SM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Importing documents

After creating the project, you need to import your data into the project.
In ATLAS.ti, data is organised into documents corresponding a single piece _unit of data_, such as an individual interview.
For ATLAS.ti Web, you can only upload textual data (`.docx`, `.docx`) and `.pdf`.
For data in other document formats, you need to use [desktop version](../atlasti_desktop) for these tasks.
For interview materials, I recommend using Microsoft Word as these files can be edited e.g. for typos within ATLAS.ti.
However, do note that any changes made to the documents in ATLAS.ti (fixing typos, anonymisation, coding) is not reflected back to the raw data files.

<iframe width="560" height="315" src="https://www.youtube.com/embed/qtlmxADwThw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Exporting project

It is possible to export ATLAS.ti Web project, which allows you to continue to work with the data and analysis on Desktop version of ATLAS.ti or store it for archival.

<iframe width="560" height="315" src="https://www.youtube.com/embed/3qAU71qM4-8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Working with data

### Coding materials

Coding takes place through selecting segments of the text to create a quotation.
**Quotations** are segments of texts connected to one or more codes.
When initially familiarising yourself with the data, just adding quotations and familiarising yourself with the data is sufficient.

<iframe width="560" height="315" src="https://www.youtube.com/embed/gRXSnmX56zg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

After initial familiarisation with the topic, one moves to add **codes** to quotations.
These codes summarise the conceptual observation, they are later used to further examine the data -- they correspond to your analysis.
The code names are shown on the right margin of the text, next to the quotations they are related to.
Quotations and codes can be overlap or be inside other quotations if that makes sense.

The ATLAS.ti also provides [tools for automated coding](#automated-coding-approaches) which may aid in the research process.
Some of these are fairly new developments from natural language processing and machine learning research community, so the academic practices around such coding are still emerging.

### Managing and organising codes

!!! tip ""
    I find it easier to conduct more extensive code management and organisation on desktop version (covered later on this document), but the web system does support code management as well.

Sometimes during the coding work you notice a problem with codes: there are typos on code names or two codes should be merged.
This is done via the **Code Manager**, available on the left side column.

<iframe width="560" height="315" src="https://www.youtube.com/embed/UxUCeOQbTB8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

!!! error "Video nyt sync with the UI."
    Current ATLAS.ti Web UI is different from this user interface.

### Sharing a project

You can share the project with someone else in project settings under `Your team`.
These new team members can code and analyse the same material you have worked on.

## Doing analysis

!!! tip ""
    These steps are easier to do with the ATLAS.ti desktop.
    Therefore, [export your project](#exporting-project) and open it on the desktop client.

### Managing and organising codes

During research project, many codes emerge.
Some of them may be the same conceptual idea, which has evolved during the work.
**Code Manager** is the interface to rename, merge, split and even remove codes.
This helps to maintain the potentially messy list of codes.

Furthermore, it is possible to define hierarchies of codes.
Any code with quotes are known as **independent codes**.
These independent codes may be **subcodes** with the help of **categorical codes**.
Alternatively, codes can be grouped into **code groups** to aggregate data into more conceptual tools.
It is also possible to change the colour of codes to help to visualise these codes.

<iframe width="560" height="315" src="https://www.youtube.com/embed/fEJD3SNtmBU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Alternatively, one can work independent codes directly.
Before doing work at code level, it is a good idea to save the document and [export it](../atlasti_desktop#exporting-project).
Sometimes an independent codes contains several different conceptual ideas and there is a need to split codes into smaller units.
Or sometimes several codes indicate the same conceptual idea and should be merged together.

<iframe width="560" height="315" src="https://www.youtube.com/embed/kZEmEh-DmsQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/kzq0jdfa9jE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

!!! error "Video not in sync with the UI."
    Current ATLAS.ti 23 may be  different from this user interface.

### From codes back to quotation

After the code stage, the analysis moves forward.
During this time, it is often necessarily to see the quotations for each code.
To access these, **quotation reader** is used.
The essential use for quotation reader is to have an easy access to your research materials based on the codes and code groups established in the prior step.

<iframe width="560" height="315" src="https://www.youtube.com/embed/bDUg8pL_H6k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Quotation reader allows to create reports of all quotations under a single code.
This can be helpful to report the data and provide summarisation of the dat and analysis.

<iframe width="560" height="315" src="https://www.youtube.com/embed/JlMzVVNKH7Q" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

!!! error "Video not in sync with the UI."
    Current ATLAS.ti 23 may be  different from this user interface.

## Advanced analysis

ATLAS.ti is a versatile environment to work with qualitative data.
Therefore, just conducting thematic classification through code management is not the only possible direction for analysis.
Rather, it is possible to develop more articulated connections between codes and documents,

### Network view

!!! error "More description needed"
    This section requires a bit more description.

The network view can help to examine how documents, quotations and codes together visually.
It allows adding more detailed relationships between codes to help on theory forming.

<iframe width="560" height="315" src="https://www.youtube.com/embed/llelw22MFeo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

!!! error "Video not in sync with the UI."
    Current ATLAS.ti 23 may be  different from this user interface.

### Co-occurance

Our research aims to make sense of emerging patterns from the data, for example identify how codes are often together (occurance) or identify how codes relate to original code.
To help in this, ATLAS.ti provides various tools.

It possible to visualise the co-occurances via **Sankey Diagram**, i.e., see which codes relate to which documents or which documets often co-occure.

<iframe width="560" height="315" src="https://www.youtube.com/embed/-3N86QAaQ0s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



### Queries

Alternative, there is a mechanism to conduct **queries** to the data, examining if codes overlap or are near-by each other.
Thus, one can examine data using combinations of codes through search interface.

<iframe width="560" height="315" src="https://www.youtube.com/embed/WlN3SwcZKkE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

!!! error "Video not in sync with the UI."
    Current ATLAS.ti 23 may be  different from this user interface.


## Automated coding approaches

### Named entity recognition

### Sentiment analysis

### AI coding

!!! error "Work in progress."
    This section is not yet ready.

<iframe width="560" height="315" src="https://www.youtube.com/embed/fyRUzAhVY_E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/wnJ9ecBJ3kc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


