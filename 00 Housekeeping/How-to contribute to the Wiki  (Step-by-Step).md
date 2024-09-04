# Contributing to the Excalidraw Wiki

Welcome to contributing to the Excalidraw Wiki! Follow these instructions to make contributions to the project.
In the example below your GitHub account name is `brave_contributor` and you are going to create a new contribution called `my-next-contribution`.
In case you get lost, consult ChatGPT.

I recommend installing GitHub Desktop as that makes some of these steps easier, though once you know the steps, it is a pretty simple and mechanic process.
## 0. Initial Preparation

### How to Fork the Repository
1. Go to the [Excalidraw Wiki repository](https://github.com/zsviczian/excalidraw-wiki) on GitHub.
2. Click the **Fork** button at the top right of the page.
3. Choose your GitHub account as the destination for the fork. This creates a copy of the repository under your account.

### How to Clone Your Fork to Your Local Device
1. Navigate to your forked repository, `https://github.com/brave_contributor/excalidraw-wiki`.
2. Click the **Code** button and copy the URL for cloning.
3. Open your terminal or command line interface.
4. Run the following command to clone the repository:
```bash
   git clone https://github.com/brave_contributor/excalidraw-wiki.git
```
5. Change to the repository directory:
```bash
   cd excalidraw-wiki
```
6. Start Obsidian, Open excalidraw-wiki as a Vault, Enable plugins.

## 1. Prepare Contribution
### Switch to the Master Branch
1. Go to the `excalidraw-wiki` folder in terminal or command prompt
2. Ensure you are on the master branch:
```bash
    git checkout master
```

### Pull Latest Changes from zsviczian/excalidraw-wiki Master
1. Add the original repository as a remote:
```bash
    git remote add upstream https://github.com/zsviczian/excalidraw-wiki.git
```
2. Fetch the latest changes from the original repository:
```bash
    git fetch upstream
```
3. Merge the changes into your local master branch:
```bash
    git pull upstream master
```

### Create and Switch to a Local Branch
1. Create a new branch for your contribution:
```bash
    git checkout -b my-next-contribution
```

##  2. After You Are Ready with the Editing
### Commit Changes to my-next-contribution
1. Stage your changes:
```bash
    git add .
```

2. Commit your changes with a descriptive message:
```bash
    git commit -m "Description of your changes"
```

### Push my-next-contribution to brave_contributor/excalidraw-wiki
1. Push your branch to your forked repository:
```bash
    git push origin my-next-contribution
```

## 3. Opening a Pull Request
1. Go to your forked repository on GitHub, https://github.com/brave_contributor/excalidraw-wiki.
2. Click on the **Compare & pull request** button that appears after pushing your branch.
3. Review the changes to ensure everything is correct.
4. Set the base repository to zsviczian/excalidraw-wiki and the base branch to master.
5. Enter a descriptive title and detailed description for your pull request.
6. Click **Create pull request** to submit your changes for review.
