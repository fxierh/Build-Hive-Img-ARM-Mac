# Build-Hive-Img-ARM-Mac

Allows building [Openshift-hive](https://github.com/openshift/hive) images on an ARM-based Mac (MBP-2021/MBA-2022 etc.) 
with a single "docker-compose up". 

Prerequisites:
1. A ./env/quay_credentials.env file which includes "username" and "password" environment variables.

Usage:
1. Change the value of the "repo" environment variable in the Dockerfile to the name of your quay.io repo for Hive !
2. docker-compose up --build

Notes:
1. This job can be a bit time-consuming, as emulation reduces code efficiency.
   Therefore, it is recommended to reserve a fair amount of computing resources to docker.
   For ex.: 8 out of 10 CPU cores + 16 out of 32 GB memory + 2 GB swap on a 32-GB MBP-2021.
