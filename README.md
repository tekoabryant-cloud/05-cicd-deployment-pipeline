# CI/CD Deployment Pipeline

## Project Overview

This project demonstrates a Continuous Integration and Continuous Deployment (CI/CD) pipeline using GitHub Actions and Python.

The pipeline automatically runs tests when code is pushed to the `main` branch or when a pull request is opened against `main`.

The purpose of this project is to demonstrate practical experience with Git, GitHub, Python testing, GitHub Actions, YAML configuration, automated testing, and CI/CD fundamentals.

## Technologies Used

- Python 3.12
- pytest
- Git
- GitHub
- GitHub Actions
- YAML

## Project Structure

    05-cicd-deployment-pipeline/
    ├── .github/
    │   └── workflows/
    │       └── ci-cd.yml
    ├── app/
    │   ├── __init__.py
    │   └── app.py
    ├── tests/
    │   └── test_app.py
    ├── .gitignore
    ├── README.md
    └── requirements.txt

## How the Pipeline Works

When code is pushed to the `main` branch or a pull request targets `main`, GitHub Actions automatically:

1. Checks out the repository.
2. Sets up Python 3.12.
3. Upgrades pip.
4. Installs the project's dependencies.
5. Runs the automated pytest test suite.

The workflow is defined in `.github/workflows/ci-cd.yml`.

## Automated Testing

The project uses pytest to test the Python application.

Tests can be run locally with:

    python -m pytest

The same test command is executed automatically by GitHub Actions.

## CI/CD Workflow

The workflow is configured to run on:

- Pushes to the `main` branch
- Pull requests targeting the `main` branch

The workflow uses GitHub Actions to create a repeatable automated testing process.

## Troubleshooting

During development, the CI pipeline initially encountered a Python package import error in the GitHub Actions environment.

The issue was resolved by adding `app/__init__.py` so Python could recognize the application directory as a package.

The test execution command was also updated from `pytest` to `python -m pytest`.

After these changes, the GitHub Actions workflow successfully completed with all tests passing.

## Skills Demonstrated

- Git and GitHub version control
- GitHub Actions
- CI/CD fundamentals
- Automated testing
- Python application structure
- YAML configuration
- Troubleshooting CI/CD failures
- Reading and interpreting error messages
- Basic DevOps practices

## Project Goals

This project was created to develop hands-on experience with automated software testing and CI/CD workflows.

It demonstrates how source code changes can automatically trigger a testing process before changes are considered ready for deployment.

## Project Status

**Completed**

The CI/CD pipeline is operational and successfully runs automated tests through GitHub Actions.

The latest GitHub Actions workflow completed successfully with a green status.