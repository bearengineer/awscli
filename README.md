# awscli

# What is awscli?

> Awscli is the Amazon web services command line interface.

[Overview of awscli](https://docs.aws.amazon.com/cli/index.html)

# TL;DR;

```bash
$ docker run -ti --rm bearengineer/awscli
```

# Supported tags and respective `Dockerfile` links

* [`1.16`, `latest` (Dockerfile)](https://github.com/bearengineer/awscli/blob/Dockerfile)

Subscribe to project updates by watching the [bearengineer/awscli GitHub repo](https://github.com/bearengineer/awscli).

# Get this image

The recommended way to get the Bear Engineer awscli Docker Image is to pull the prebuilt image from the [Docker Hub Registry](https://hub.docker.com/r/bearengineer/awscli).

```bash
$ docker pull bearengineer/awscli:latest
```

To use a specific version, you can pull a versioned tag. You can view the [list of available versions](https://hub.docker.com/r/bearengineer/awscli/tags/) in the Docker Hub Registry.

```bash
$ docker pull bearengineer/awscli:[TAG]
```

If you wish, you can also build the image yourself.

```bash
$ docker build -t bearengineer/awscli:latest 'https://github.com/bearengineer/awscli.git#master'
```

# Configuration

## Running commands

To run commands inside this container you can use `docker run`, for example to execute `aws s3 ls` you can follow the example below:

```bash
$ docker run --rm --name awscli bearengineer/awscli:latest -- aws s3 ls
```

Consult the [AWS CLI Reference Documentation](https://docs.aws.amazon.com/cli/index.html) to find the completed list of commands available.

## AWS Credentials

AWS credentials can either be passed by environment variables, or by mounting a volume with aws credentials file under `/root/.aws`.

### Environment variables

```bash
$ docker run -ti -e 'AWS_ACCESS_KEY_ID=********************' -e 'AWS_SECRET_ACCESS_KEY=****************************************' --rm bearengineer/awscli aws s3 ls
```

### AWS directory

```bash
docker run -ti -v '/Users/bearengineer/.aws:/root/.aws' --rm bearengineer/awscli aws s3
```

# Contributing

We'd love for you to contribute to this container. You can request new features by creating an [issue](https://github.com/bearengineer/awscli/issues), or submit a [pull request](https://github.com/bearengineer/awscli/pulls) with your contribution.

# Issues

If you encountered a problem running this container, you can file an [issue](https://github.com/bearengineer/awscli/issues). For us to provide better support, be sure to include the following information in your issue:

- Host OS and version
- Docker version (`docker version`)
- Output of `docker info`
- Version of this container
- The command you used to run the container, and any relevant output you saw (masking any sensitive information)

# License

Copyright (c) 2019 Bear Engineer. All rights reserved.

This work is licensed under the terms of the MIT license.  
For a copy, see <https://opensource.org/licenses/MIT>.

