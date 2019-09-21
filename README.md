# GitHub Actions for DDLC Mods

This is a CI template to get you started on automated builds using GitHub Actions.

GitHub Actions is a brand new tool announced by GitHub to write workflows to automate a lot of tasks on GitHub, ranging from continuous integration builds to adding comments on pull requests made by first-time contributors.

> Note: At time of writing, GitHub Actions is still in private beta.

## Using GitHub Actions

To get started, drag the `scripts` directory and the `.github/workflows` directory to the root of your repository project. Feel free to take a look at `build.yml` to see how writing a workflow is done!

Most of the hard work is done for us through custom actions written by both Sayo-nika and Project Alice.

## Configuration

Most of the steps in the workflow should already set for you to use. In most cases, modifying the "Set up mod for build" step is all that's needed:

```yml
- name: Set up mod for build
  shell: bash
  run: |
    mkdir mod
    rm -rf sample_mod/stein/README.html && cp -vRf sample_mod/stein/* mod/
```

Additionally, you can add other steps and actions to customize the workflow to your needs. This may even include running the linter.

> For more information, consult GitHub's documentation on Actions here: [https://help.github.com/en/categories/automating-your-workflow-with-github-actions](https://help.github.com/en/categories/automating-your-workflow-with-github-actions)
