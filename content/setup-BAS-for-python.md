# Setup SAP Business Application Studio and a dev space
> [SAP Business Application Studio](https://help.sap.com/docs/bas/sap-business-application-studio/what-is-sap-business-application-studio) is based on Code-OSS, an open source project used for building Visual Studio Code. Available as a cloud service, SAP Business Application Studio provides a desktop-like experience similar to leading IDEs, with command line and optimized editors.

> At the heart of SAP Business Application Studio are the dev spaces. The dev spaces are comparable to isolated virtual machines in the cloud containing tailored tools and preinstalled runtimes per business scenario, such as SAP Fiori, SAP S/4HANA extensions, Workflow, Mobile and more. This simplifies and speeds up the setup of your development environment, enabling you to efficiently develop, test, build, and run your solutions locally or in the cloud.

## Open SAP Business Application Studio
👉 Go to your [BTP trial account](https://account.hanatrial.ondemand.com/trial/#/home/trial).

👉 Navigate to `Instances and Subscriptions` and open `SAP Business Application Studio`.

![Open BAS](images/BTP_cockpit_BAS.png)


## Create a new Dev Space for CodeJam exercises

👉 Create a new Dev Space.

![Create a Dev Space 1](images/bas.png)

👉 Enter the name of the Dev space `AIEscapeRoom`, select the `Basic` kind of application and `Python Tools` from Additional SAP Extensions.

👉 Click **Create Dev Space**.

![Create a Dev Space 2](images/create_dev_space.png)

You should see the dev space **STARTING**.

![Dev Space is Starting](images/dev_starting.png)

👉 Wait for the dev space to get into the **RUNNING** state and then open it.

![Dev Space is Running](images/dev_running.png)

## Clone the exercises from the Git repository

👉 Once you opened your dev space in BAS, use one of the available options to clone this Git repository with exercises using the URL below:

```sh
https://github.com/noravth/AI-escape-room.git
```

![Clone the repo](images/clone_git.png)

👉 Click **Open** to open a project in the Explorer view.

![Open a project](images/clone_git_2.png)

## Open the Workspace

The cloned repository contains a file `escaperoom.code-workspace` and therefore you will be asked, if you want to open it. 

👉 Click **Open Workspace**.

![Automatic notification to open a workspace](images/open_workspace.png)

☝️ If you missed the previous dialog, you can go to the BAS Explorer, open the `codejam.code-workspace` file, and click **Open Workspace**.

You should see:
* `AIEscapeRoom` as the workspace at the root of the hierarchy of the project, and
* `ai-escape-room` as the name of the top level folder.

👉 You can close the **Get Started** tab.

![Open a workspace](images/workspace.png)


## Create a virtual environment and install the Python SDK for SAP HANA Cloud

👉 Start a new Terminal.

![Extensions to install](images/start_terminal.png)

👉 Create a virtual environment using the following command:

```bash
python3 -m venv ~/projects/generative-ai-codejam/env --upgrade-deps
```

👉 Activate the `env` virtual environment like this and make sure it is activated:

```bash
source ~/projects/generative-ai-codejam/env/bin/activate
```

![venv](images/venv.png)


👉 We will also need the [HANA client for Python](https://pypi.org/project/hdbcli/).

```bash
pip install --require-virtualenv hdbcli
```
