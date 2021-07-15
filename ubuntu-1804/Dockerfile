FROM octopuslabs/workertools:latest-ubuntu.1804

# Get Terraform
# https://computingforgeeks.com/how-to-install-terraform-on-ubuntu-centos-7/
RUN curl -fsSL https://apt.releases.hashicorp.com/gpg | apt-key add - && \
    apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main" && \
    apt-get update && apt-get install terraform -y

# Get AWS CLI
# https://docs.aws.amazon.com/cli/latest/userguide/install-linux.html#install-linux-awscli
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && \
    ./aws/install && \
    rm awscliv2.zip && \
    rm -rf ./aws

# Get ECS CLI
# https://github.com/aws/amazon-ecs-cli
RUN curl --silent --location "https://amazon-ecs-cli.s3.amazonaws.com/ecs-cli-linux-amd64-latest" -o /usr/local/bin/ecs-cli && \
    chmod +x /usr/local/bin/ecs-cli

RUN pwsh -c 'Install-Module -Force -Name AWS.Tools.Installer -AllowClobber -Scope AllUsers'

RUN pwsh -c 'Install-Module -Force -Name AWS.Tools.Common -AllowClobber -Scope AllUsers'