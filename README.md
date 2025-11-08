# Template Repo

This is a template repo to set up some basic aider ai coding stuff. It sets up the format so that I can easily spin up more new repos with the relevant context

## Documentation

LLMs rely heavidly on prompts and context to understand the task. The best way to achieve this is through good documentation. Doing so will help ensure the model has the correct context, and therefore performs correctly.

### Readme.md.template
Fill this out with the details of the specific repo and then replace this README at the root of the repo. 
```bash
mv README.md.template README.md
```

### Contributions.md

Style and programming guidelines for the model to use when creating code.


### Current_status.md 

A writeup of the current status of the project (useful for if you'll be leaving the project for a bit and need to come back). Can help the model pick back up where the headspace was at last time. 

## Aider files

### .aider.conf.yml

This file sets up the basic configs of the aider chat. With it you can select the model to use and files to add in. By default it adds in the README and Contributions files as readonly to set the model context. 

### .env 

This file holds the API keys to initialize the local system (without accidentally exposing secrets)

To use it, create a copy of the .env.template file, fill out the API key secrets, then source the env file using export_env

```bash
cp .env.template .env
# input API key
source .env
```


## Coding workflow

This is a recommendation on how to use the workflow:
1. Set up workspace (env file, model, configs, etc...)
2. activate aider
3. Pull in context of current_status into aider
4. code
5. update documentation and current_status
6. profit