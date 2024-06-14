## DevopsCI

This repository contains my homework for a DevOps course, focusing on implementing Continuous Integration using GitHub Actions. The project is structured to build and test a C++ application using CMake and Google Test.

### GitHub Actions Workflow

The `cmake.yml` file located in `.github/workflows/` defines the CI workflow for this project. The workflow is triggered on pushes and pull requests to the `task-ci` branch.

#### Workflow Steps

1. **Checkout Repository**: Uses the `actions/checkout@v3` action to checkout the repository.
2. **Download GTest**: Clones the Google Test repository and copies it to the `task-ci/3rdparty/` directory.
3. **Configure CMake**: Configures the CMake build system in the `task-ci/build` directory.
4. **Build**: Builds the project using the configured CMake build system.
5. **Upload Artifacts**: Uploads the build artifacts (binaries and libraries) to GitHub.

### CMake Configuration

The `task-ci/CMakeLists.txt` file configures the CMake build system for the project. It sets the runtime and library output directories and includes the necessary subdirectories for building the project.

### Getting Started

To get started with this project, clone the repository and ensure you have CMake and a C++ compiler installed. You can then build the project locally using the following commands:

```sh
cd task-ci
mkdir build
cd build
cmake ..
cmake --build .
```

### Running Tests

To run the tests locally, you can use the following command after building the project:

```sh
cd task-ci/build
ctest
```
