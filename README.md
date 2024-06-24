# Kubernetes Operators Test

This repository contains a set of tests for evaluating Kubernetes operators during the upgrade process. The tests cover various aspects of operator functionality and best practices.

## Overview

Updating a Kubernetes operator in a production environment can be challenging, especially when users have created objects managed by it. The deployment of a new operator version might lead to application crashes during reconciliation due to incompatible Custom Resource Definitions (CRDs), risky rollouts, and other issues. To prevent such negative impacts on the objects, we have developed a comprehensive set of tests for various Kubernetes operators. These tests ensure that the upgrade process proceeds smoothly and as expected.

## Prerequisites

- Kubernetes cluster (version 1.23 or higher)
- [KUTTL](https://kuttl.dev/docs/#install-kuttl-cli) v0.14.0 or higher

## Running the Tests

1. Clone the repository
1. Run `kubectl kuttl test path/to/operator-folder`

## License

This project is licensed under [Apache 2.0](https://github.com/snapp-incubator/operators-test/blob/main/LICENSE).
