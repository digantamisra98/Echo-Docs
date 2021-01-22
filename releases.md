---
description: History of Releases of Echo
---

# Releases

## 0.1.4 - 2021-01-XX  🌙

_**Upcoming Stable Release. Currently under development.**_

### Fixed

* Fixed implementations for the following activation functions in **PyTorch**: `Swish`, `SILU`, `ESwish`, `Flatten T-Swish`, `ELiSH`, `Hard ELiSH`, `BReLU`, `APL` 
* Fixed Unit Tests for **PyTorch** activation functions
* Fixed **Flake8** and **Black** support
* Fixed Codecov support

### Changed

* Changed documentation support from **Sphinx** \(**Readthedocs**\) to **Gitbook**. Former is now depreciated.
* Changed Issues and PR templates
* Changed directory listing for `Activation/`
* Updated package dependencies graph
* Removed dedicated smoke test and unit test folder
* Refactored Unit Tests for activation functions
* Removed activation functions with no published paper reference
* New logo for Echo

### Added

* Added support for **MegEngine**
* Added **isort** and **autoflake** into the code styling framework
* Added proper documentation in **Gitbook**.
* Added `FReLU` activation function. 
* Added DCO agreement
* Added [Contributing Guidelines](https://xa9ax.gitbook.io/echo/contributing-guidelines)
* Added `GELU` for **TensorFlow**
* Added Project Roadmap
* Added Attention Models for NLP and CV
* Added Optimizers
* Added Unit tests for attention models
* Added Rosenbrock and Himmelblau convergence tests for optimizers

## [0.1.3 - 2019-08-15](https://pypi.org/project/echoAI/0.1.3/) 🌕

_**Current Stable Release**_

### Fixed

* Fixed documentation issues with support for linting tools - **Black** and **Flake8** was added
* Fixed implementation for `Mish` activation function

### Changed

* Added support for more activation functions
* Documentation was updated

## [0.1.2 - 2019-08-11](https://pypi.org/project/echoAI/0.1.2/) 🌑

_**First Stable Release**_

### Added

* Introduced novel activation functions with support for PyTorch and TensorFlow
* Concise documentation via Sphinx on Readthedocs was made available

_\*\*\*\*_

