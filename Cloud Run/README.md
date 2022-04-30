# Cloud Run deployment

---
marp: true
title: Project - Python with GCP 
paginate: true 
theme: gaia
---

# Project - Python with GCP

---

# 1. Cloud Run

## Steps for Deployment

- Create a New Project in GCP Console associated with the correct billing account.
- Create a Empty git repository
- The created repositiry mainly follows the flask file structure. Its looks like below figure.
<img width="372" alt="Screen Shot 2022-04-30 at 11 58 12 AM" src="https://user-images.githubusercontent.com/98420519/166115323-d03519ba-9278-4056-814d-8a309b0be542.png">

- From the above structure Dockerfile and cloudbuild.yaml are the mandetory files for automating the complete process.
---
- To create docker image and push to your GCP project we follow the below commands:
    - docker build .
    - docker images
- Initially, when we run the docker images command we will have the repository as <None>, tag as latest, image id as some value, created as hrs/days/months, size as amount of size used.
- Copy the latest image id and paste it in the command below:
[docker tag <latest-image-id> gcr.io/[project id]/[project name]]
- Now when we give the above command repository name and docker image will be allocated. 
---
- To configure docker authentication after logging into gcloud, we run the below command:
[gcloud auth configure-docker]
- First, we need to enable the conatiner registry and cloud build.
- 


