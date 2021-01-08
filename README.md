# Jenkins pipeline test with shared library
This repository contains the main code to perform tasks `build`, `database`, `deploy`, `test` inside Jenkins pipeline. Pipeline code and supplementary functions implemented in separate repo and can be found [here](https://github.com/baurzhansiit/common-lib.git).

## Setup your Jenkins before playing with this Repo

- Jenkins -> Manage Jenkins -> Configure System -> Search: Global Pipeline Libraries (repo for shared library can be found [here](https://github.com/baurzhansiit/common-lib.git))

## quick overview

1. Jenkins pipeline job will trigger Jenkinsfile 
2. Jenkinsfile will point to shared library (which was configured in the previous step)
3. Jenkins will pick up declarative.groovy file with pipeline code inside and run according to stages and steps by triggering functions inside pipelineConfig.groovy to pass data from myconfig.yml file
4. if some steps will fail you will receive email notification with some useful information about the failure.
