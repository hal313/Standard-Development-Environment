<!--- Version 1.0.1 -->

# standard-development-environment-example

> This is the "standard development environment example".

## Purpose

The "standard development environment" example is a POC which demonstrates how to support a locally running instance of a complex environment. In this example, a number of servers are required to run (web servers as well as back-end servers).

For convenience, an online IDE is included.

An "environment generator" is included to allow users to custom-create an environment.

### Sub Applications

The concept of the sub application is to allow a modular system whereby applications are loaded dynamically (perhaps by availability or user roles).

While a simple application loader is implemented in this example, the entire system has a non-opinionated approach to loaders. Put simply, any HTML/JavaScript/CSS loader can work.

A "main loader" web page is rendered to the client browser; this is implemented as [html-01](https://github.com/hal313/html-01) and includes supporting JavaScript and CSS styling.

In this example, each sub application is defined by a JavaScript file; the sub application may augment the existing HTML. For instance, [html-02](https://github.com/hal313/html-02) will load an additional piece of functionality - the "reverse" button.

## Usage

Generally speaking, a user uses the [environment generator](https://hal313.github.io/dev-env/) to download a Docker configuration or startup script. The generated environment allows for users to run the entire environment locally while adding an online IDE to allow simple changes.

More details can be found on the [generator site](https://github.com/hal313/dev-env#usage).

## Git Modules

This repository is mostly a tracking repository which uses git modules. [This primer](https://www.vogella.com/tutorials/GitSubmodules/article.html#creating-repositories-with-submodules) shows basic usage.

## TODO
Currently, only one environment can exist on a host system because container names are not dynamically referenced in the proxy configuration (the generator does support prefix/suffix naming of containers).

- [GitHub issue](https://github.com/hal313/reverse-proxy/issues/1)
- [Explanation](https://github.com/hal313/dev-env#todo)
