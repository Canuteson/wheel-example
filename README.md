Wheel Example
=============

Example building an application as a wheel using wheel-builder Docker container

### Setup

Create a virtualenv and install dependencies:

    . build/venv/bin/activate
    virtualenv build/venv

Install dependencies:

    pip install -r requirements.txt

### Build

Run wheel builder, mounting your application source directory to /application and your Wheel destination to /wheelhouse:

    docker run --rm -v "$(pwd)"/wheelexample:/application -v "$(pwd)"/build:/wheelhouse wheel-builder

### Install

Install your wheel into your venv:

    pip install --no-index -f build WheelExample


See Dockerfile for an example running the wheel via Docker

