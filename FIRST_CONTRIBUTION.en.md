# Guide for beginning contributors

## Index

- [How to contribute?](#how-to-contribute)
  - [1º Step](#1º-step) - Fork
  - [2º Step](#2º-step) - Cloning
  - [3º Step](#3º-step) - Add link to official repository
  - [4º Step](#4º-step) - Create a branch to contribute
  - [5º Step](#5º-step) - Add and commit a contribution
  - [6º Step](#6º-step) - Submit the branch with the contribution to the fork
  - [7º Step](#7º-step) - Make a Pull requets from the branch to the official project
- [Contribution approved, what to do?](#contribution-approved-what-to-do?)
  - [Deleting old branch locally](#deleting-old-branch-locally)
- [Synchronizing the fork/clone with the official repository](#synchronizing-the-fork/clone-with-the-official-repository)
  - [Sync the clone](#sync-the-clone)
  - [Sync the fork](#sync-the-fork)
- [Useful links](#useful-links)

## How to contribute?

To make contributions, make sure you have [git](https://git-scm.com/) installed in your environment.

With **git** already installed, follow the steps below.

### 1º Step

**Fork** the repository to your account by clicking the fork button:

![image](https://user-images.githubusercontent.com/50463866/103658686-4cd2f500-4f4a-11eb-9f9d-3ba714bfc815.png)

You will be redirected to your account once the process is complete.

### 2º Step

Once you have the repository in your account, **clone** it in your local environment:

```bash
$ git clone https://github.com/<YOUR_ACCOUNT_NAME>/<REPOSITORY_NAME>.git
```

### 3º Step

With the clone in your environment, link the local repository to the remote [Coding in Community](https://github.com/Coding-in-community) organization:

```bash
$ git remote add upstream https://github.com/Coding-in-community/<REPOSITORY_NAME>.git
```

This will serve to sync updates made in the official repository to your local environment.

> OBS: This command is only necessary to run once after cloning.

To check if everything went right, run the command below in the terminal:

```bash
$ git remote --v
```

If everything went well, there should be an output similar to this:

```bash
origin  https://github.com/<YOUR_ACCOUNT_NAME>/<REPOSITORY_NAME>.git (fetch)
origin  https://github.com/<YOUR_ACCOUNT_NAME>/<REPOSITORY_NAME>.git (push)
upstream        https://github.com/Coding-in-community/<REPOSITORY_NAME>.git (fetch)
upstream        https://github.com/Coding-in-community/<REPOSITORY_NAME>.git (push)
```

### 4º Step

Create a **branch** to make your contribution:

```bash
$ git checkout -b feature/feature_name
```

Now add your contributions to the project.

### 5º Step

Add your contributions:

```bash
$ git add example_file.js
```

> OBS: Add all files/directories created and/or modified

Now **commit**:

```bash
$ git commit -m "Contribution Description"
```

### 6º Step

After completing your contribution, send it to the remote repository in your account:

```bash
$ git push origin feature/feature_name
```

### 7º Step

In your github account, submit a **Pull Request** with your contribution to the official repository:

![image](https://user-images.githubusercontent.com/50463866/103661883-0089b400-4f4e-11eb-8752-3c341fdc3e4a.png)

Now wait for the review from one of the project's maintainers.

## Contribution approved, what to do?

After an approved pull request, if you don't want to contribute again, you can either delete the branch you used to contribute on the Pull Request page itself or delete the fork from your account.

If you want to make other contributions that are unrelated to the branch of the old contribution, delete the old one and create a new one.

### Deleting old branch locally

Go to the default branch:

```bash
$ git checkout master
```

Delete the old one:

```bash
$ git branch -d name_of_old_branch
```

Now create a new branch and repeat the steps [4º Step](#4º-step), [5º Step](#5º-step), [6º Step](#6º-step) and [7º Step](#7º-step)

## Synchronizing the fork/clone with the official repository

To synchronize the fork/clone with the new features you have in the official repository follow the steps below:

### Sync the clone

Make sure you're on the default branch, which commonly is `master`:

```bash
$ git checkout master
```

Now, sync with:

```bash
$ git pull upstream master
```

After that, the local environment is synchronized.

### Sync the fork

Now that the local environment is synchronized, synchronize the remote too:

```bash
$ git push origin master
```

Ready, local and remote environment synchronized with the official.

## Useful links

If you have any questions about a command used or just want to understand better, see one of the links below:

- [Git documentation](https://git-scm.com/docs)
