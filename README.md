# Dockerfile Build Failure: Missing or Incorrect Requirements File

This repository demonstrates a common error when building Docker images: specifying a `requirements.txt` file that doesn't exist or is in the wrong location.

## Bug

The provided `Dockerfile` attempts to install Python dependencies using `pip3 install -r requirements.txt`. However, the `requirements.txt` file is either missing from the context or in an unexpected location.

## Solution

The solution involves ensuring the `requirements.txt` file exists in the correct location within the Docker context and is correctly referenced in the `Dockerfile`.

## Reproduction Steps

1. Clone this repository.
2. Try to build the Docker image using the original `Dockerfile`.
3. Observe the error.
4. Build the image again using the `Dockerfile.fixed` which is the fixed version.
