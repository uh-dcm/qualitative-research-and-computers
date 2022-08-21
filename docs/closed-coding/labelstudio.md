# Label Studio

[Label Studio](https://labelstud.io/) is a free/open source tool aimed at data annotation, i.e., humans making observations on data.
It is highly flexible: images, audio and text data can be annotated with it.
In this brief tutorial we focus on the most simple type of annotation work and ask coders to choose the most suitable category for a piece of text.

## Installation

Closed-coding task is a collaborative task: all coders must access the same data and use exactly the same codes for this.
Label Studio makes this easy: it is an web-based app coders can access with their web browsers.
However, this requires the system to be installed on a web server.

Finnish universities have access to computing resources, including web servers via [CSC](https://csc.fi/).
These services are available without additional charge.

### Setting up user account to CSC

1. Login to [my.csc.fi](https://my.csc.fi/) with your Haka user account. This will create a CSC user account for you.
1. Login to [rahti.csc.fi](https://rahti.csc.fi:8443/) wuth your newly created CSC user account.

### Setting up a web service project

1. On Rahti management interface, create a new project with a unique name (such as `username-labelstudio`) and display name of your choice (for example `LabelStudio`) and a brief description (`LabelStudio for course Qualitative Research and Computers`) and click Create.
    ![Create project step one](../assets/labelstudio_rahti_create_project_1.png)
    ![Create project step two](../assets/labelstudio_rahti_create_project_2.png)
1. Move to the project page of the just created project.
1. On storage page, create a new storage called `data` with 1 Gib of memory, click Create.
    ![Open storage page](../assets/labelstudio_rahti_volumes.png)
    ![Create volume](../assets/labelstudio_rahti_volume_create.png)
1. On dashboard page, choose to deploy image with the image name `heartexlabs/label-studio:latest`
    ![Open dashboard](../assets/labelstudio_rahti_dashboard.png)
    ![Choose to deploy image](../assets/labelstudio_rahti_create_deployment_1.png)
    ![Type in image name](../assets/labelstudio_rahti_create_deployment_2.png)
1. Once created, edit the deployment and add environment values, finally save
    * `HOME` value of `/tmp/`
    * `DATABASE_NAME` value of `/data/database.sqlite3`
    * `LABEL_STUDIO_BASE_DATA_DIR` value of `/data`
    ![Options for deployment](../assets/labelstudio_rahti_edit_deployment_1.png)
    ![Edit deployment](../assets/labelstudio_rahti_edit_deployment_2.png)
    ![Edit environment variables](../assets/labelstudio_rahti_edit_environment.png)
1. From configurations, add storage to the project and mount it to `/data`
    ![Open configurations](../assets/labelstudio_rahti_configurations.png)
    ![Click add storage](../assets/labelstudio_rahti_add_storage_1.png)
    ![Enter mount name correctly](../assets/labelstudio_rahti_add_storage_2.png)
1. Wait a few minutes
1. From the dashboard click Add Route and Create a new route (all settings are OK).
    ![Open dashboard](../assets/labelstudio_rahti_dashboard.png)
    ![Add rote](../assets/labelstudio_rahti_add_route_1.png)
1. The site now shows a new link where your freshly installed Label Studio is.
    ![See link](../assets/labelstudio_rahti_url.png)

## Setting up Label Studio

1. Create an user account on Label Studio instance
1. Once logged in, create a new project
1. Give the project a name and description

### Data import

Data may contain both entries to be classified and metadata, such as origins or timestamps of entries.
They are formulated into a spreadsheet, where different columns divide the entries.
You can use spreadsheet software, such as Microsoft Excel, to produce the file, but you [must save the data as a `.csv` file](https://support.microsoft.com/en-us/office/save-a-workbook-to-text-format-txt-or-csv-3e9a9d6c-70da-4255-aa28-fcacf1f081e6).

In case that there is no metadata involved, entries can also be on a text file (`.txt`, not `.docx`), where each unit is on its own line.

### Codebook setup

Under the menu "Labelling setup", there are several templates pre-made for content labelling.
We focus on text classification, so choose from the templates "Natural Language Processing" and from there, "Text Classification".
(To get an idea of the versatility of Label Studio, you should check out all the templates.)

The template customisation user interface allows you to define the **codebook**, that is, the alternatives from which the coder must choose the code from.
New choises can be entered by typing them to the "Add choice" text box and adding them, and codes can be removed by clicking the grey X on the right side of alternatives.
Note that the choice can be longer than one word, even to the degree of sentences or short paragraph.
You can see the coding interface on right side Preview panel.

![See link](../assets/labelstudio_template_customisation.png)

Label Studio does allow customisation of the labelling interface beyond these templates using its own [markup language](https://labelstud.io/tags/).

## Coding content on Label Studio

On the project dashboard, press the blue "Label All Tasks" button to start coding.
You will be automatically directed to the coding user interface you have customised and imported data is shown unit by unit.

!!! warning "By default, Label Studio is open to internet"
    On current setup anyone on the internet is able to create new user account as well.
    If you use label studio for research purposes, limit this by adding following environment variables during project setup (we left them out as that stage is already cumbersome). (For details, see [user guide](https://labelstud.io/guide/signup.html#Restrict-signup-for-cloud-deployments).)
    ```
      LABEL_STUDIO_DISABLE_SIGNUP_WITHOUT_LINK=true
      LABEL_STUDIO_USERNAME=<username>
      LABEL_STUDIO_PASSWORD=<password>
    ```

    Even after limiting access to Label Studio, bear in mind that every user on Label Studio has access to all data and projects on the server.
    This is due to their business model, where more extensive securing of the system is for paying [enterprise customers only](https://labelstud.io/guide/security.html).

### Inviting new coders for the project.

With closed coding approach, academic researchers want have several coders to code each unit.
This way, it is possible assess intercoder reliability and evaluate the objectivity (i.e., agreement) between codes.
As we are using a non-enterprise version of Label Studio, there is no easy way to increase the minimum number of labels per project, it is automatically set as one.

To overcome this technical limitations, setup a separate project for each coder.
Follow steps described above to create new projects.

New coders can create an user account to your label studio and access all projects through the interface.
Just share them the link to your instance.

!!! info
    It is also possible manually to enter several codes per unit on Label Studio.
    Open each entry separately and by choosing the user name of the person, you may click "Create Annotation" -- but as you would need to do this manually for each unit, it is highly cumbersome.

## Assessing intercoder reliability

To assess the intercoder reliability, export the coded data from all projects (i.e., the project you coded and the project your partner coded).
Use the CSV format and open them.

Check that both spreadsheets are in the same order, i.e., units (rows) are the same.
(These sheets contain the IDs, which allows you to order them.)
Create a new spreadsheet where you copy assigned codes for each unit, so that each coder has their own column.
Find and replace data so that codes are transformed into numeric values.
The final outcome looks like this:

![Coding data on spreadsheet](../assets/spreadsheet_recal2.png)

Use software such as [ReCal2](http://dfreelon.org/utils/recalfront/recal2/) to calculate the intercoder reliability score for the coded data from this new spreadsheet.
Remember to code the data per requirements of the software, for ReCal2 remove all headers and the column containing data so that only codes (as numbers) for all coders remain on the spreadsheet.
