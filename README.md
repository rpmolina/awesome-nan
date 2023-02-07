<!--lint disable double-link awesome-heading awesome-git-repo-age awesome-toc-->

<div align="center">
<p>
    <img
        style="width: 200px"
        width="200"
        src="https://avatars.githubusercontent.com/u/4426989?s=200&v=4"
    >
</p>
<h1>Awesome NaNLABS</h1>

[Changelog](#) |
[Contributing](./CONTRIBUTING.md)

</div>
<div align="center">

[![Continious Integration][cibadge]][ciurl]
[![License: MIT][licensebadge]][licenseurl]

</div>

This repository contains different infrastructure components, CI/CD pipelines, automation tools
among other resources that are used in different projects here at [NaN Labs](https://www.nanlabs.com/).

## Contents

- [Applications](#applications)
- [Examples](#examples)

  - [DevOps](#devops)
    - [A/B Testing](#ab-testing)
    - [Shell Scripting and Utilities](#shell-scripting-and-utilities)
    - [Continuous Integration, Delivery and Deployment](#continuous-integration-delivery-and-deployment)
    - [Containers, Orchestration and Serverless](#containers-orchestration-and-serverless)
      - [Containers and Compositions (Docker, Docker Compose, Buildpacks and more)](#containers-and-compositions-docker-docker-compose-buildpacks-and-more)
      - [DevContainers and Codespaces](#devcontainers-and-codespaces)
      - [Kubernetes](#kubernetes)
    - [Infrastructure as Code](#infrastructure-as-code)
      - [AWS Amplify](#aws-amplify)
      - [Serverless Framework and CloudFormation](#serverless-framework-and-cloudformation)
    - [Node Package Managers](#node-package-managers)
  - [Frontend](#frontend)
    - [React State Management](#react-state-management)

- [Contributing](#contributing)
- [Contributors](#contributors)

## Applications

- [Complete AWS Glue ETL](https://github.com/nanlabs/devops-reference/tree/main/examples/_apps/serverless-glue/) - A complete example of an AWS Glue application that uses the [Serverless Framework](https://www.serverless.com/) to deploy the infrastructure and DevContainers and/or Docker Compose to run the application locally with AWS Glue Libs, Spark, Jupyter Notebook, AWS CLI, among other tools. It provides jobs using Python Shell and PySpark.
- [Golang REST API boilerplate](https://github.com/nanlabs/nancy.go/tree/main/examples/golang-todo-rest-crud/) - REST API to create, update and retrieve Entities, including grateful shutdown, rate limiting, structured logging, unit tests, integration tests, environment variables, health check and API documentation with swagger. Technologies: Golang 1.19, MongoDB (with Docker Compose), Gorilla Mux, Go Swagger, Tollbooth (rate limiting), Zap (logging), Viper, Mockery, Makefile, Pre-commit, and DockerTest (integration tests).
- [React Webpack Boilerplate](https://github.com/nanlabs/react-webpack-boilerplate) - A simple boilerplate to start a React project with Webpack. Boilerplate generated using [create-react-webpack-project](https://www.npmjs.com/package/create-react-webpack-project) contains full CI/CD setup with GitHub Actions and Docker. It also contains a full local development setup with hot reload and production ready setup with minification and optimization. It also contains a full test setup with Jest and React Testing Library.
- [Storybook Playground](https://github.com/nanlabs/nancy.js/tree/main/apps/playground/) - This app was created with the goal to have examples of ours React components, hooks and libraries that are created in different packages in the repository Nancy.js.

## Examples

### DevOps

#### A/B Testing

- [AWS CloudWatch Evidently](https://github.com/nanlabs/devops-reference/tree/main/examples/services/aws-cloudwatch-evidently/) - A complete analysis of the service and a Proof of Concept on how to integrate it with a Node.js application.
- [Feature flags post](https://www.atlassian.com/continuous-delivery/principles/feature-flags) - How to progressively expose your features with feature flags by IAN BUCHANNAN.

#### Shell Scripting and Utilities

- [Bash as a Wrapper Utility](https://github.com/nanlabs/devops-reference/tree/main/examples/scripts/bash-as-a-wrapper-utility-basic/) - Bash as a wrapper utility for other languages and tools.
- [Bash as a Wrapper Utility with Easy Options](https://github.com/nanlabs/devops-reference/tree/main/examples/scripts/bash-as-a-wrapper-utility-with-easy-options/) - Bash as a wrapper utility for other languages and tools using Easy Options.
- [Easy Options](https://github.com/nanlabs/devops-reference/tree/main/examples/scripts/easy-options/) - Easy options for shell scripts.
- [When to use shell](https://google.github.io/styleguide/shellguide.html#when-to-use-shell) - A guide from Google on when to use shell scripts.

#### Continuous Integration, Delivery and Deployment

- [Actionlint Playground](https://rhysd.github.io/actionlint/) - Static checker for GitHub Actions workflow files.
- [Automation Seed example](https://github.com/nanlabs/automation-seed/tree/main/.github/workflows) - Different workflows to validate the code and deploy an automation report page.
- [Markdown Lint](https://github.com/nanlabs/devops-reference/tree/main/.github/workflows/markdownlint.yml) - This workflow validates the Markdown files in the repository using the [markdownlint action](https://github.com/marketplace/actions/markdown-lint).
- [React Webpack Boilerplate](https://github.com/nanlabs/react-webpack-boilerplate/tree/main/.github/workflows) - Different workflows to validate the code and deploy a React application.
- [Shell Check](https://github.com/nanlabs/devops-reference/tree/main/.github/workflows/shellcheck.yml) - This workflow validates the shell scripts in the repository using the [shellcheck action](https://github.com/ludeeus/action-shellcheck).
- [Terraform Check](https://github.com/nanlabs/devops-reference/tree/main/.github/workflows/tf-check.yml) - This workflow validates the Terraform files in the repository using the [terraform action](https://github.com/dflook/terraform-fmt-check).
- [Todo to Issue](https://github.com/nanlabs/devops-reference/tree/main/.github/workflows/todo.yml) - This workflow scans new commits on the main branch looking for `TODO`s in the code and creates new GitHub issues.

#### Containers, Orchestration and Serverless

##### Containers and Compositions (Docker, Docker Compose, Buildpacks and more)

- [Airflow and Spark environment using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/docker/airflow/) - Dockerfile and docker-compose.yml to run Airflow locally with initialization scripts.
- [AWS Glue using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/docker/glue/) - Dockerfile and docker-compose.yml for AWS Glue development with AWS Glue Libs, Spark, Jupyter Notebook, AWS CLI among other tools.
- [AWS Neptune using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/docker/neptune/) - Dockerfile and docker-compose.yml to run AWS Neptune locally with initialization scripts.
- [Localstack using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/docker/localstack/) - Dockerfile and docker-compose.yml to run Localstack locally with all the necessary services. This example also includes a script to create the necessary resources in Localstack. The provided examples are for DynamoDB, S3, SQS and Kinesis.
- [Microsoft SQL Server using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/docker/mssql/) - Dockerfile and docker-compose.yml to run Microsoft SQL Server locally with initialization scripts.
- [MongoDB + Mongo Express using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/docker/mongodb/) - Dockerfile and docker-compose.yml to run MongoDB and Mongo Express locally with initialization scripts.
- [PostgreSQL using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/docker/postgres/) - Dockerfile and docker-compose.yml to run PostgreSQL locally with initialization scripts.
- [Python Buildpack](https://github.com/nanlabs/devops-reference/tree/main/examples/buildpacks/python#readme) - Buildpack example for Python applications.

##### DevContainers and Codespaces

- [AWS Glue](https://github.com/nanlabs/devops-reference/tree/main/examples/devcontainers/glue/) - DevContainer for AWS Glue development. Uses `docker-compose` to run VSCode attached to a container with all the necessary tools to develop AWS Glue jobs such us AWS Glue Libs, Spark, Jupyter Notebook, AWS CLI among other tools.
- [Node.js](https://github.com/nanlabs/devops-reference/tree/main/examples/devcontainers/nodejs/) - DevContainer for Node.js development. Uses `docker-compose` to run VSCode attached to a container with all the necessary tools to develop Node.js applications.

##### Kubernetes

- [Ingress](https://github.com/nanlabs/devops-reference/tree/main/examples/kubernetes/ingress/) - Ingress example using NGINX Ingress Controller. You can run this example locally using [Minikube](https://minikube.sigs.k8s.io/docs/start/).

#### Infrastructure as Code

##### AWS Amplify

- [AWS Amplify + NextJS 13](https://github.com/nanlabs/devops-reference/tree/main/examples/amplify/amplify-nextjs-deployment/) - AWS Amplify example to deploy a NextJS v13 application to the Cloud.

##### Serverless Framework and CloudFormation

- [AWS AppSync + Python](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless/serverless-appsync-python/) - Serverless Framework example to deploy an AWS AppSync API using Python. It also has a local development environment using [Serverless Offline](https://www.serverless.com/plugins/serverless-offline).
- [AWS AppSync + TypeScript](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless/serverless-appsync-nodejs/) - Serverless Framework example to deploy an AWS AppSync API using TypeScript. It also has a local development environment using [Serverless Offline](https://www.serverless.com/plugins/serverless-offline).
- [AWS Glue with Python Shell and PySpark Jobs](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless/serverless-glue/) - Serverless Framework example to deploy an AWS Glue job using Python Shell and PySpark.
- [DocumentDB Cluster](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless/serverless-documentdb/) - Serverless Framework example to deploy a DocumentDB cluster with all the necessary resources.
- [Neo4j in EC2](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless/serverless-neo4j-ec2/) - Serverless Framework example to deploy a Neo4j instance in EC2.
- [RDS Postgres Instance](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless/serverless-rds-postgres/) - Serverless Framework example to deploy a RDS Postgres cluster with all the necessary resources.
- [Serverless Middy](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless/serverless-middy/) - Serverless Framework example to deploy a lambda function using [Middy](https://middy.js.org/), the stylish Node.js middleware engine for AWS Lambda.
- [Serverless Middy with Custom Middleware](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless/serverless-middy-custom-middleware/) - Serverless Framework example to deploy a lambda function using [Middy](https://middy.js.org/), the stylish Node.js middleware engine for AWS Lambda.
- [Serverless S3 Local](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless/serverless-s3-local/) - Serverless Framework example to run a lambda function locally using [Serverless S3 Local](https://www.serverless.com/plugins/serverless-s3-local).

#### Node Package Managers

- [Node Package Managers](https://github.com/nanlabs/nancy.js/tree/main/examples/node-package-managers/) - Comparison of the most popular Node Package Managers: npm, yarn, pnpm.

### Frontend

#### React State Management

- [AgileTs](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/atomic-agilets/) - This example shows how to use AgileTs to manage state.
- [Akita](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/reactive-akita/) - This example shows how to use Akita to manage state.
- [Context](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/hooks-context/) - This example shows how to use React Context to share data between components.
- [Effector](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/reactive-effector/) - This example shows how to use Effector to manage state.
- [Global State](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/hooks-global-state/) - This example shows how to use a global state using React Hooks.
- [Hookstate](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/hooks-hookstate/) - This example shows how to use Hookstate to manage state.
- [Jotai](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/atomic-jotai/) - This example shows how to use Jotai to manage state.
- [MobX](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/bidirectional-mobx/) - This example shows how to use MobX to manage state.
- [MobX State Tree](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/bidirectional-mobx-state-tree/) - This example shows how to use MobX State Tree to manage state.
- [Prop Drilling](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/hooks-prop-drilling/) - This example shows how to pass data from a parent component to a child component using props.
- [React Easy State](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/bidirectional-easy-state/) - This example shows how to use React Easy State to manage state.
- [React Query](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/api-react-query/) - This example shows how to use React Query to fetch data from an API.
- [Recoil](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/atomic-recoil/) - This example shows how to use Recoil to manage state.
- [Redux Toolkit](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/unidirectional-redux-toolkit/) - This example shows how to use Redux Toolkit to manage state.
- [Rematch](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/unidirectional-rematch/) - This example shows how to use Rematch to manage state.
- [Rxjs](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/reactive-rxjs/) - This example shows how to use Rxjs to manage state.
- [Storeon](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/reactive-storeon/) - This example shows how to use Storeon to manage state.
- [Teaful](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/hooks-teaful/) - This example shows how to use Teaful to manage state.
- [Unistore](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/unidirectional-unistore/) - This example shows how to use Unistore to manage state.
- [Valtio](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/bidirectional-valtio/) - This example shows how to use Valtio to manage state.
- [XState](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/fsm-xstate/) - This example shows how to use XState to manage state.
- [Zustand](https://github.com/nanlabs/nancy.js/tree/main/examples/state-management/examples/unidirectional-zustand/) - This example shows how to use Zustand to manage state.

## Contributing

- Contributions make the open source community such an amazing place to learn, inspire, and create.
- Any contributions you make are **truly appreciated**.
- Check out our [contribution guidelines](./CONTRIBUTING.md) for more information.

## Contributors

<a href="https://github.com/nanlabs/awesome-nan/contributors">
  <img src="https://contrib.rocks/image?repo=nanlabs/awesome-nan"/>
</a>

Made with [contributors-img](https://contrib.rocks).

[cibadge]: https://github.com/nanlabs/awesome-nan/actions/workflows/ci.yml/badge.svg
[licensebadge]: https://img.shields.io/badge/License-MIT-blue.svg
[ciurl]: https://github.com/nanlabs/awesome-nan/actions/workflows/ci.yml
[licenseurl]: https://github.com/nanlabs/awesome-nan/blob/main/LICENSE
