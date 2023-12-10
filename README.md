# Using Markdown and Git for Documentation

## Table of Contents

- [Requirements](#requirements)
  - [Software](#software)
  - [Account](#account)
- [Create Repository](#create-repository)
- [Clone Repository Locally](#clone-repository-locally)

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
