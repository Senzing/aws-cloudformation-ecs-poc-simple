# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
[markdownlint](https://dlaa.me/markdownlint/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.5.0] - 2021-03-16

### Added in 0.5.0

- Use of `SENZING_G2CONFIG_GTC` and `senzing/g2configtool`

### Changed in 0.5.0

- "[Truth Set](https://s3.amazonaws.com/public-read-access/TestDataSets/SenzingTruthSet/truth-set.json)" now used as sample data.
- Formatted JSON for easier modification
- Updated docker image versions:
  - public.ecr.aws/senzing/init-container:1.6.8
  - public.ecr.aws/senzing/sshd:1.1.0

## [0.4.0] - 2021-03-12

### Added in 0.4.0

- Added `slow_start.duration_seconds`
- Optional importing of sample data

### Changed in 0.4.0

- stream-producer now specifies `SENZING_DEFAULT_DATA_SOURCE` and `SENZING_DEFAULT_ENTITY_TYPE`
  - Removed from stream-loader
- Updated to senzingapi-2.4.1-21064
- Updated docker image versions:
  - public.ecr.aws/senzing/stream-loader:1.7.2
  - public.ecr.aws/senzing/stream-producer:1.4.0
  - public.ecr.aws/senzing/xterm:1.1.0

## [0.3.0] - 2021-02-26

### Added in 0.3.0

- Support for "WithInfo" Queue.

## [0.2.10] - 2021-02-19

### Changed in 0.2.10

- Updated docker image versions:
  - public.ecr.aws/senzing/init-container:1.6.6
  - public.ecr.aws/senzing/redoer:1.3.5
  - public.ecr.aws/senzing/senzing-api-server:2.3.2
  - public.ecr.aws/senzing/stream-loader:1.7.1
  - public.ecr.aws/senzing/stream-producer:1.3.3
  - public.ecr.aws/senzing/xterm:1.0.5
  - public.ecr.aws/senzing/yum:1.1.4

## [0.2.9] - 2021-02-17

### Changed in 0.2.9

- Add parameter acknowledging an insecure system.

## [0.2.8] - 2021-02-16

### Changed in 0.2.8

- Docker image URL changed from `public.ecr.aws/d5v4a2g3` to `public.ecr.aws/senzing`

## [0.2.7] - 2021-02-10

### Added in 0.2.7

- `SENZING_SKIP_DATABASE_PERFORMANCE_TEST` environment variable set in Xterm and Sshd containers.
  Already exists in Stream-loader.

## [0.2.6] - 2021-02-08

### Added in 0.2.6

- Change from DockerHub-based image registry to AWS-ECR-based registry

## [0.2.5] - 2021-02-05

### Added in 0.2.5

- Added `/var/opt/senzing` access to `senzing/stream-producer`

## [0.2.4] - 2021-02-03

### Added in 0.2.4

- `SshUsername` output variable

### Changed in 0.2.4

- Updated to latest Docker images
  - senzing/init-container:1.6.5
  - senzing/stream-loader:1.7.0
  - senzing/stream-producer:1.3.1
  - senzing/entity-search-web-app:2.2.1
- Changed output variable names to collate better
  - `ApiServerHeartbeatUrl` is now `UrlApiServerHeartbeat`
  - `JupyterUrl` is now `UrlJupyter`
  - `SwaggerUrl` is now `UrlSwagger`
  - `WebAppUrl` is now `UrlWebApp`
  - `XtermUrl` is now `UrlXterm`
- Modified host in URLs from `senzing.github.io` to `hub.senzing.com`

## [0.2.3] - 2021-01-21

### Fixed in 0.2.3

- Changed ARN references
- Added AccountID output

## [0.2.2] - 2021-01-05

### Fixed in 0.2.2

- Modified DependsOn values
- Disabled Public IP addresses

## [0.2.1] - 2021-01-04

### Fixed in 0.2.1

- Modified DependsOn values
- Disabled Jupyter by default.  Keeps crashing.
- Added missing Tags

## [0.2.0] - 2020-12-31

### Added to 0.2.0

- Support Senzing database cluster
- Autoscale Senzing API Server and Entity Search Web App
- Generate random password for SSHD container
- Remove Key/Value pairs that specify default values

## [0.1.0] - 2020-12-30

### Added to 0.1.0

- Base functionality
- For testing, all services active
- Single AWS Aurora Postgres Serverless database
