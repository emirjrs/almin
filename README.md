# Project Title

A node.js example todo app with drone.io integration for CI/CD demo

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.
We are going to bring up an application container

- Clone this repository
- cd to repo folder
- Ensure you're in Develop branch
```bash
git branch
git checkout develop
```
- Execute drone.io locally for build & test
```bash
drone exec
```
- If you ant to deploy locally: Bring up app container, please use absolute path to cloned repository, then add examples/todomvc to the path (we need to mount this folder as a volume in the local container)
```bash
docker run -it -v [/your/path/to/cloned/repository/]examples/todomvc:/app:ro -p 8080:8080 emirjrs/node:v2
```
- Check in your browser http://localhost:8080

### Prerequisites
- Git
- Github account (https://github.com/)

#### For local deployments only
- Docker (https://www.docker.com)
- Internet access to docker hub (https://hub.docker.com/)
- drone.io cli (https://docs.drone.io/cli/install/)

### CI/CD --> drone.io cloud

Any change pushed to the repository will trigger build, test & deploy (only in master branch) in drone.io cloud. You visualize these CI/CD stages in ypur browser:
```
https://cloud.drone.io/emirjrs/almin
```

Please, push some changes and then verify URL above.


## Managing CI/CD

* .drone.yml

* Dockerfile

Both of them in project repository

## Deployment

Deployment stage is only executed when changes are pushed to master branch, it simulate how would be a deployment in any cloud provider, since drone.io would be for build and testing, for real deployments a drone.io plugin could be configured for deploy in majors clouds provider.

## Built With

* [Almin](https://github.com/almin/almin) - Application code forked from
* [Drone.io](https://cloud.drone.io/emirjrs/almin) - CI/CD
* [Docker](https://cloud.docker.com/repository/docker/emirjrs/node/general) - Images por deploying locally and testing drone.io cloud

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **emirjrs** - *Initial work* - [CI/CD demo](https://github.com/emirjrs/almin)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* God & Family
* almin (https://github.com/almin/almin)
* CI/CD best practices
