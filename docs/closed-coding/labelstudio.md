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
