# Using Markdown and Git for Documentation

## Table of Contents

- [Purpose](#purpose)
- [Requirements](#requirements)
  - [Software](#software)
  - [Account](#account)
- [Create Repository](#create-repository)
- [Clone Repository Locally](#clone-repository-locally)
- [Working on your Document](#working-on-your-document)
  - [Main Page](#main-page)
  - [Set Tab Spacing](#set-tab-spacing)
  - [Help from Visual Studio Code](#help-from-visual-studio-code)
    - [Problems](#problems)
    - [File Unsaved](#file-unsaved)
    - [Preview](#preview)
- [Commiting your Changes](#committing-your-changes)
- [Extras](#extras)
  - [Editing Directly in GitHub](#editing-directly-in-github)
  - [Mermaid Diagrams and Charts](#mermaid-diagrams-and-charts)

## Purpose

Utilizing [Markdown language](https://www.markdownguide.org/) and [Git](https://git-scm.com/) for documentation, provides the following benefits:

- All changes to the document through its entire lifecycle are tracked.
- Free and Open Source.
- Documentation can be saved offsite and shared world-wide if wanted, though services like [GitHub](https://github.com/).
- Markdown can be converted into a website if desired using static website generators such as [Hugo](https://gohugo.io/).
- Provides practical learning path for modern development source control with Git.

## Requirements

### Software

- The following free software will be required.

  - [Git Client](https://git-scm.com/downloads)
    - If installing for the first time, please be sure to configure your identity for the client.  This can be done by using the commands below in a PowerShell window, for more details see the documentation [here](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).

      ```gitbash
      git config --global user.name "John Doe"
      git config --global user.email johndoe@example.com
      ```

  - [Visual Studio Code](https://code.visualstudio.com/download)
    - In Visual Studio Code, click on the **Extensions** button and search for **markdownlint by David Anson**, then click on **Install**.  This will provide us Markdown syntax warnings and errors, live while making a document.

      ![VSCode Markdownlint extension](/images/VSCode-MarkdownlintExtension.png)

### Account

- An account to a Git cloud-based service provider will be required. For the purposes of this document [GitHub](https://github.com/) is utilized.

## Create Repository

The following steps will be utilized to create a Git repository, in which the documentation will be created. All your documentation can be combined into one repository or a separate repository created for each document, such organization is a matter of personal taste.

- Using your web browser of choice, browse to [https://github.com](https://github.com) and sign-in with your account.
- Once in your GitHub account, select **Repositories** on the top bar.
- When on the **Repositories** page, click on the green button **New**.
- On the **Create a new repository** page, set the following items:
  - **Repository Name**: Can be anything you wish that is meaningful to those who will use it.
  - **Description**: Optional, but recommended to describe the purpose of the repository.
  - **Public/Private**:  This is the most important decision to make, do you wish your documentation to be visible to the entire world or private just to yourself and those you may specifically grant access.
  - **Add a README file**: Check this box to provide us the base file in which to create our documentation and also provides you a built-in example.
  - **Add .gitignore**: Leave the default None for this use case.
  - **Choose a license**: Setting a license is optional, though is highly recommended if you have the repository set to **Public**.  For example this documentation is set to [Creative Commons Zero v1.0 Universal](https://choosealicense.com/licenses/cc0-1.0/), which dedicates this documentation's use to the public domain.
- Click on **Create repository**.

    ![NewGitRepo](/images/GitHub-NewGitRepo.png)

## Clone Repository Locally

- Start by ensuring you have Visual Studio Code open and are logged into your GitHub account in your browser.
- In **GitHub** ensure you are on the main page for the repository you created in the previous section [Create Repository](#create-repository).
- Click on the green **Code** button, then copy the **HTTPS** path.

  ![GitHub-HttpsClone.png](/images/GitHub-HttpsClone.png)

- In **Visual Studio Code** in the left tool bar, click on the source control icon.

  ![VSCode Source Control Button](/images//VSCode-SourceControlButton.png)

- In the Visual Studio Code Source Control panel, click on **Clone Repository**.

  ![VSCode Clone Repository](/images/VSCode-CloneRepo.png)

- In the top bar, it will now ask you to provide the URL source.  Paste in the **HTTPS** path you copied for your **GitHub** repository.

  ![VSCode Clone Repository URL](/images/VSCode-CloneRepoURL.png)

- You will now be prompted to select where you which to locally clone the repository. I suggest creating a folder **C:\Git**, though you may use any location of your choosing.

  > **NOTE:** If you are using a private repository, Visual Studio code will prompt you to sign-in to your GitHub account so it may make the connection to your repository. It will save the credentials securily for future use.

## Working on your Document

### Main Page

The main starting file for your documenation will be the **README.md** file, which already contains Markdown language from the GitHub new repository template. If desired you can examine it to begin learning the syntax, then when ready dive in and delete the contents of the file to start your own document.

The **.md** file extension, is used for all **Markdown language** files.  The **README.md** file is special in that it will automatically be displayed as the main page in a GitHub repository.

> **NOTE:** The basics of Markdown Syntax can be found at [https://www.markdownguide.org/basic-syntax/](https://www.markdownguide.org/basic-syntax/)

### Set Tab Spacing

Markdown language utilizes two spaces when indenting.  To help facilitate this, use the following steps to set your tab spacing.

- In the bottom left panel, you will find a section called **Spaces**.

  ![VSCode Spaces Panel](/images/VSCode-SpacesSetting01.png)

- Left-Click on **Spaces**, doing so will present a **Select Action** menu at the top of Visual Studio Code.  For this option, select **Indent Using Spaces**.

  ![VSCode Spaces Type Selector](/images/VSCode-SpacesSetting02.png)

- A new selector menu will now appear for **Select Tab Size for Current File**, select the value of **2**.

  ![VSCode Tab Size Selector](/images/VSCode-SpacesSetting03.png)

- In the bottom left panel, you should now see **Spaces: 2**.

### Help from Visual Studio Code

As you write, Visual Studio Code can provide you assistance with the following features.

#### Problems

> **NOTE:** The Problems feature will utilize data from the Markdown Lint Extension.  It's installation was covered in the [Software](#software) section.

- In the top menu select **View** and then click on **Problems**.

  ![VSCode View Problems](/images/VSCode-ViewProblems.png)

- Now in a Problems window at the bottom of Visual Studio Code, you will see live listings of any Markdown syntax issues. The issues will also provide a link to find more information on each item and how to correct it.

  ![VSCode Problems](/images/VSCode-Problems.png)

#### File Unsaved

Visual Studio Code will indicate on each tab, with a dot, any files which have been modified and not yet saved. Additionally, if there are syntax issues in your file it will alter the colour of the file name.

  ![VSCode Tab Indicators](/images/VSCode-TabIndicators.png)

#### Preview

In order to view a live preview of your changes as you work, follow the following step.

- **Right-click** the **Tab** for your file **README.md** and select **Open Preview**.  This will open a new tab, in which you will see the redered version of what your document will look like once committed to GitHub.

### Committing your Changes

As you make changes and save your file, you will notice an indicator appears on the source control icon.

  ![VSCode Changes Indicator](/images/VSCode-ChangesIndicator.png)

When ready to commit your changes, ideally every time you complete a logical section, you would perform the following steps.

- Left-Click on the **Source Control Icon**.
- At the top of the **Source Control Panel**, enter a **Message** briefly describing what the change contains.
- Left-Click on the **Commit** button.

> **NOTE:** Your first time Visual Studio Code may ask you if you would like to Auto Stage all your changes, select **Yes**.

- The button will now change to **Sync Changes**.

  ![VSCode Sync Changes](/images/VSCode-SyncChanges.png)

- Left-Click on **Sync Changes**, to upload all your current changes to your GitHub account.

  > **NOTE:** The first time Visual Studio code may prompt you to sign-in to your GitHub account so it may make the connection to your repository. It will save the credentials securily for future use.

- In your browser go to your GitHub account and open the repository for your document.  There you should now see the document you just synced.

## Extras

### Editing Directly in GitHub

All of the editing for this document was done using Visual Studio Code on desktop. However, if desired it is also possible to edit directly in GitHub. This is done by browsing to the file you wish to edit in GitHub, then clicking the Edit Icon button. You may also choose **github.dev** which is a web-based version of Visual Studio Code.  However, you can lose some functionality for extensions with the web-based version.

  ![GitHub Edit](/images/GitHub-Edit.png)

### Mermaid Diagrams and Charts

Diagraming and charts through text definitions is also possible, with the use of [Mermaid](https://mermaid.js.org/intro/). Adding the capability to preview them in Visual Studio Code, is done by adding the extension **Markdown Preview Mermaid Support by Matt Bierner**.

For example, the following block of code generates the diagram displayed:

  ````markdown
  ```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
  ```
  ````

  ```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
  ```
