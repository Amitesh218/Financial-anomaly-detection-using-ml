# Financial-anomaly-detection-using-ml
Simple financial anomaly detection using models trained on multiple machine learning algorithms.

The project aims to showcase the usage of machine learning models for financial fraud detection, although in the current stage it is very rough and unimpressive.

## Setting up tools
I'll be using docker for the entire setup, to make things easier and to isolate the operation. (Also cause i didn't try anything else)

*Docker desktop*

To install docker desktop, head to [their website]([https://www.docker.com/](https://www.docker.com/products/docker-desktop/)) and select the appropriate version.

*Docker*

Open a terminal and enter the following command. This will only install docker and not docker desktop, which provides the gui interface. If you prefer to work with the gui, refer the previous step.

*linux! cause i haven't used windows or mac to work on this. so if youre one of em, i'd suggest you js go with docker-desktop*

`sudo pacman -S docker`

note that you need to type the name of the package manager used by your distro

the dataset used here is [Synthetic financial datasets for fraud detection](https://www.kaggle.com/datasets/ealaxi/paysim1)

- now make a directory named "financial_anomaly" in the home directory and in the root directory
- also, download and keep a copy of the dataset in both the directories
- make a docker-compose file in the financial_anomaly directory IN the root directory
- copy the contents from the docker-compose file in the repo and paste it
- open a terminal in the directory and run
`docker-compose up --build`

you now have the containers needed for the model training running!

- to proceed with using jupyter notebook, open a web browser and open localhost:8888
- copy and paste the token generated during the containers building to login
- open the /work directory and start making python notebooks! (or, yknow js copy and paste the stuff from the repo)
- oh and don't forget to run them too.. cause like- programs don't run by themselves

you'll get the outputs of the csv files in the financial_anomaly directories
if you cant find em in one, make sure to check the other... Yeah, i know, not very demure. But i cant be bothered. If it works, don't fix it ykwim

## Shutting down and reopening

*docker desktop*

shut down the docker engine, DUH or stop the containers using the ui

*docker*

just type `docker-compose down` on a terminal

this could be a problem when working with multiple other containers but i don't think anyones ever gonna read this anyways so imma just let it be
actually no nvm im curious now
okay so a quick google search fetched me the results:
`docker container stop [OPTIONS] CONTAINER [CONTAINER...]`

use this to stop specific containers

to restart all of this,
js open a terminal in a directory with the docker-compose file and run

`docker-compose up`

> (also youre gonna have to copy paste the token every time... haha... if it aint broke, dont fix it amirite!)
