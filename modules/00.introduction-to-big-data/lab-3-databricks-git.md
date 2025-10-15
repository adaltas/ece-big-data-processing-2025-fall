---
duration: 1h
category:
  - name: LAB
platforms:
  - name: Databricks  
  - name: Github  
  - name: Gitlab  
revisions:
  - date: 2025-10-09
    comment: Initial writing
    author: joe@adaltas.com
tags:
  - name: TUTORIAL
---
# Lab: Utilize Databricks Git Folders

Databricks provides an API and visual client that allows users to integrate Git repos within a Databricks workspace. Users can utilize many common Git operations including push, pull, branch management, diff, etc. This allows for better source control and colaboration on projects directly in the Databricks workspace. The lab will guide users through configuring a new Git project on Databricks.  

## Objectives

- Create a new Databricks Git integration project

## Tasks

1. Git provider configuration (easy level)
2. Databricks Git Folders configuration (easy level)
3. Databricks Git UI utilization (easy level)
4. Databricks notebook Git command utilization (easy level)

## Prerequisites

- An existing Databricks workspace
- An existing account on a Git provider such as Github or Gitlab
- Familiarity with Git and basic Git commands

## Part 1. Git provider configuration

A new repository is created on a chosen Git provider such as [Github](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository) or [Gitlab](https://docs.gitlab.com/user/project/). Databricks Git folders can be configured to use public or private repositories. **Note:** This step can be skipped if there is an existing repository users wish to integrate with Databricks. Once repository has been choosen or created, it is neccasary to configure an access token. Steps will differ depending on the Git provider.  

### Github personal access token configuration

[Personal access tokens (classic)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#personal-access-tokens-classic) or [Fine-grained personal access tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#fine-grained-personal-access-tokens), but fine-grained access tokens are prefered.  

After signing into Github, click on the user icon in the upper right hand corner and select settings from the drop down.

[Acces settings menu]()

On the settings page scroll down and select the `< > Developer settings` option.  

[< > Developer settings]()

Expand the `Personal access tokens` menu and select `Fine-grained tokens`.  

[Fine-grained tokens]()

On the right hand side click `Generate new token`.

[Generate new token]()

Configure the token name. Token names must be unique and should be named such that they are easy to manage and track, such as the repository they have access to or the application that is using the token in the case that multiple repositories are being accessed. The default expiration date of 30 days may be changed as desired.  

[Token name and expiration]()

Configure the repository access. In general, it is recommended to follow the principles of least privilege and scope the token to access only select repositories.

[Repo access]()

Configure the repository permissions. Click `Add permissions` and search for `contents`. Github automatically adds the required `Metadata` permission.

[permissions]()

Select `Read and write` from the drop down menue (Databricks integration will require both), and click 'Generate token`.

[access]()

A new access token is generated. **Note:** Remember to add the token to a chosen password manager as the token cannot be seen again once navigating away from the page. 

[token]()

## Gitlab

A Gitlab [personal access token](https://docs.gitlab.com/user/profile/personal_access_tokens/) will be configured for Databricks projects. According to the Databricks [documentation](https://docs.databricks.com/aws/en/repos/get-access-tokens-from-git-provider#gitlab) it is also possible to use [project tokens](https://docs.gitlab.com/user/project/settings/project_access_tokens/) but there have been [issues reported](https://community.databricks.com/t5/data-engineering/gitlab-integration/m-p/92989/highlight/true#M38602) utilizing project access tokens. Users may attempt to do project access tokens if their Gitlab allows for it but may end up falling back to personal access tokens.  

After signing into Gitlab click on the user icon near the top left and select `Preferences`.  

[preferences selection]()

Select the `Personal access tokens` from the menu on the left.  

[Preferences]()

Click add new token and configure the token name. Token names are not required to be unique, but, giving tokens unique names will make tokens easier to manage and track. The default expiration date of 30 days may be changed as desired.  

[token name and expiration]()

Databricks will require read and write access to the repository. In `Select scopes` select the `write_repository` to enable read and write permissions, and then click `Create token`.  

[gitlab read write]()

A token will be generated. **Note:** Make sure the token is saved somewhere like a password manager as it cannnot be accessed after navigating away from the page.  

[personal access tokens page]()

## Part 2: Databricks Git Folders configuration

Databricks access to the Git provider is first configured by linking accounts. After logging in to the Databricks account, click on the user icon in top right hand corner and select `settings` from the drop down menu. 

[db account settings]()

In the settings menu, select the `Linked Accounts` option.  

[settings menu]()

Select `Add Git credential`. Select the chosen provider and the `Personal access token` option. Fill in the provider email or username, paste the token and click save.

[credential creation]()

After the Git provider account has been linked, navigate to `Workspace > Users`. Inside the users directory, click `Create` and select `Git folder` from the drop down.  

[databricks git folder]()

In the `Create Git folder`, past the url for the desired repo and indicate the correct Git provider. Provide a Git folder name. It is not required that the name of the folder in Databricks match the Git repository name, but this is the best choice for the majority of the cases.

[create folder]()
