# Deploying a NodeJS docker image to a Kubernetes cluster with your Shippable pipeline.

![AyeAye](https://github.com/devops-recipes/deploy-kubernetes-basic/raw/master/public/resources/images/captain.png)

This repository demonstrates the following :
- Setup CI for a NodeJS application that builds a docker image and deploys it to DockerHub.
- Setup a CD pipeline to deploy the docker image to a Kubernetes cluster using a manifest job and deploy job.

## Prerequisites to run this sample

* Source control account (e.g. GitHub, Bitbucket, Gitlab)
* Shippable account (sign up for free at www.shippable.com)
* Kubernetes cluster.

## Setup
* Fork this repo into your local repository in your source control account.
* Login into Shippable with your source control account(wwww.shippable.com).
* Create a [Docker Hub integration](http://docs.shippable.com/integrations/imageRegistries/dockerHub/) on shippable to your docker hub.
* All your CI configuration is in `shippable.yml` file, while you will modify to reflect your integration.
* Update the integrationName in the integration.hub section with the integration name created above.
* Change the DOCKER_REPO and DOCKER_ACC to point to your repo and docker account.
* Next, follow these [CI Setup Instructions](http://docs.shippable.com/ci/runFirstBuild/) to enable your forked project for CI.
* Build your CI project by clicking on the build button.
* Create the Kubernetes integration using instructions provided [here]().

##Add the pipeline  in Shippable
* Sign in with your shippable account, select your subscription from the dropdown menu in upper left (three horizontal lines).
* Select the Pipelines tab.
* Select the "+" icon in the upper right.
* Select the source control repo where your fork is. This will render all the jobs in the Single pane of glass (SPOG).
* Run the pipeline following instructions [here]().

## CI Console Output
![CI Console Output](https://github.com/devops-recipes/deploy-kubernetes-basic/raw/master/public/resources/images/console.jpg)

##Build link
[CI build on Shippable](https://app.shippable.com/github/devops-recipes/deploy-kubernetes-basic/runs/7/1/console)

##Build status badge
[![Run Status](https://api.shippable.com/projects/58fcef822ddacd090044cf75/badge?branch=master
)](https://app.shippable.com/github/devops-recipes/deploy-kubernetes-basic)


## Pipeline View
![Pipeline](https://github.com/devops-recipes/deploy-kubernetes-basic/raw/master/public/resources/images/pipeline-view.png)

## Deploy job View
![Deploy](https://github.com/devops-recipes/deploy-kubernetes-basic/raw/master/public/resources/images/deploy-job-view.png)
