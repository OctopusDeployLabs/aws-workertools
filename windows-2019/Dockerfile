# escape=`

FROM octopuslabs/workertools:latest-windows.2019
SHELL ["powershell", "-Command"]

# Install Terraform
RUN choco install terraform -y --no-progress

# # Install AWS CLI
RUN choco install awscli -y --no-progress

# # Install ECS CLI
RUN choco install ecs-cli -y --no-progress; `
    refreshenv