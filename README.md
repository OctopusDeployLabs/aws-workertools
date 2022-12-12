# AWS Worker Tools

This repository contains images that contain the tooling necessary to to use the execution container feature with Octopus Deploy when running commands against AWS.

- AWS CLI
- AWS ECS
- AWS EKS CTL
- TerraForm
- AWS PowerShell Tools Common

The following images are built in this repo:

- Ubuntu 22.04
- Ubuntu 20.04 (tagged `latest` in [DockerHub](https://hub.docker.com/r/octopuslabs/aws-workertools/tags?page=1&name=latest))
- Windows 2019 (tagged `latest` in [DockerHub](https://hub.docker.com/r/octopuslabs/aws-workertools/tags?page=1&name=latest))

A new image will be built each time a new version of AWS CLI is created.  The version numbers will be based on the version of AWS CLI.

**Please consider this repository provided as is.  If there are any issues please do not contact support.**
