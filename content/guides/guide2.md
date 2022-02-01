+++
title = "Guide 2"
date = "2022-02-01T14:40:09+01:00"
author = "Patrik"
authorTwitter = "" #do not include @
cover = ""
keywords = ["intro", ""]
description = "Intro about guide 2"
showFullContent = false
readingTime = false
+++

CEEnter API Caller
---
The API Caller is an example GUI which helps generating the proper API syntax.
Ultimately it may also execute the API call, but not at this stage yet.
The metadata for API Caller is under the api-caller folder.
The first file is the menu-map.json where the interactive menu options are defined.

## Build
Create a build using the command gradle
Because this is a prototype, the test code is not currently maintained. 
Therefore, it is necessary to call build with skipped tests.
```
./gradlew build -x test
```
To prepare for distribution
```
./gradlew distZip
```

## Run - locally
For experiments on the local computer, the program can be run as follows
For experiments on the local computer, the program can be run as follows:
1. run ```git clone << address of this git repo >>```
2. go to folder ```cd << project folder >>``` eg ```cd CEEnterCaller```
3. build see above
4. ```unzip build/distributions/ceeredhat-0.0.1.zip```
5. go to folder wuth binary eg ```cd ceeredhat-0.0.1/bin```
6. and run ```./ceeredhat```

## Docker image
To create a docker image, run the following in the project folder
```
docker build -f docker/Dockerfile.jvm -t chytrik/ceeredhat .
```
To run a local image using the docker engine eg
```
docker run -i --rm -p 8080:8080 chytrik/ceeredhat
```
