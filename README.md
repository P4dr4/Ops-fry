# Ops-fry (Resume of Github Actions)

## What is Github Actions 

    - GitHub Actions is a continuous integration and continuous delivery (CI/CD) 
    platform that allows you to automate your build, test, and deployment pipeline.

    - GitHub provides Linux, Windows, and macOS virtual machines to run your workflows,
    or you can host your own self-hosted runners in your own data center or cloud
    infrastructure.

## The components of GitHub Actions

### Workflow : 
    
    - A workflow is a configurable automated process that will run one or more jobs.

    1. Workflows are defined by a YAML file checked in to your repository and will
    run, when triggered by an event in your repository, or they can be triggered
    manually, or at a defined schedule.

### Event :

    - An event is a specific activity in a repository that triggers a workflow run.

    1. For example, activity can originate from GitHub when someone creates a pull request, 
    opens an issue, or pushes a commit to a repository. You can also trigger a workflow to 
    run on a schedule, by posting to a REST API, or manually.

### Job :
    
    - A job is a set of steps in a workflow that is executed on the same runner. 
    
    1. Each step is either a shell script that will be executed, or an action 
    that will be run. 
    
    2. Steps are executed in order and are dependent on each other. Since each 
    step is executed on the same runner, you can share data from one step 
    to another. 
    
    3. For example, you can have a step that builds your application, followed 
    by a step that tests the application that was built.

### Action :
    
    - An action is a custom application for the GitHub Actions platform, that performs 
    a complex but frequently repeated task. 
    
    1. Use an action to help reduce the amount of repetitive code that you write in
    your workflow files. An action can pull your git repository from GitHub, set up 
    the correct toolchain for your build environment, or set up the authentication to 
    your cloud provider.

### Runner :
    
    - A runner is a server that runs your workflows when they're triggered. 
    
    1. Each runner can run a single job at a time. GitHub provides Ubuntu Linux,
    Microsoft Windows, and macOS runners to run your workflows; each workflow run 
    executes in a fresh, newly-provisioned virtual machine. GitHub also offers 
    larger runners, which are available in larger configurations.

```mermaid
graph TD;
  Event-->Workflow-->Jobs-->Steps-->Action
  Workflow-->Runner-->Jobs;