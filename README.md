# Azure CI/CD Pipeline for Google Cloud Plataform Apigee Projects

This repository contains the configuration for a Azure CI/CD pipeline that automates the deployment of Apigee projects using Azure Pipelines. The pipeline includes stages for setting the deployment environment, running linting tests, manual approval, and deployment.

## Pipeline Stages

1. **Set Environment**
   - Defines the Apigee organization and environment based on the Git branch.

2. **Test Lint**
   - Runs `Apigeelint` and `ESlint` to ensure code quality.

3. **Approval**
   - Includes a manual validation step for specific branches.

4. **Deploy**
   - Installs necessary tools and dependencies.
   - Generates a GCP Service Account bearer token.
   - Executes Maven tasks to configure and deploy Apigee bundles.

## Parameters

- `memory_maven`: Memory options for Maven.
- `version_java`: Java version.
- `jdk_Version_Option`: JDK version option.
- `maven_Pom_File`: Path to the Maven POM file.

## Environment Variables

- `APIGEE_ORG`: Apigee organization.
- `APIGEE_ENV`: Apigee environment.
- `COMMIT_BRANCH`: Git branch being built.

## Usage

To use this pipeline configuration in your project, you need to have Azure Pipelines set up and configured. You can then copy the YAML configuration into your pipeline definition file.


## Tools Used

- `Azure Pipelines`: CI/CD tool.
- `ApigeeLint`: Linter for Apigee proxies.
- `ESlint`: Linter for JavaScript.
- `Node.js`: Runtime for executing scripts.
- `Maven`: Build automation tool for Java.
- `GCP (Google Cloud Plataform)`: For authentication and obtaining tokens.

### How to Run

- Clone the repository.
- Set up the required environment variables.
- Run the pipeline in Azure Pipelines.

  
### Contribution

- Fork the project.
- Create a branch for your feature (git checkout -b feature/new-feature).
- Commit your changes (git commit -am 'Adds new feature').
- Push the branch (git push origin feature/new-feature).
- Create a new Pull Request.
