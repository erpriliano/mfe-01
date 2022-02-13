# Microfrontend Experiment

This repo is created as a learning curve for microfrontend architecture. 

## What's inside ?
Within this repo, you can find :
- Container App --> Used as a HOST to decide when and where for each of sub-apps to be shown
- Products App --> Will render list of products using faker plugin
- Cart App --> Will render numbers of products in your cart, using faker plugin

## Integration 
This repo use run-time integration, which means that the container (HOST) will get access to sub-apps **AFTER** it gets loaded in the browser

## Things to notes
1. Using ModuleFederationPlugin in webpack config to access each apps
2. In every index.js of the sub-apps, you can see that I'm using `import(...)` to import bootstrap.js, this is important to run the code asynchronously, so each sub-apps can still run without error in isolation

## How to use ?
Simply clone the repo to your local, and do `yarn install` in every sub-apps 
