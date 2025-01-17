# Introduction

[**Software Contributor Documentation Table of Contents**](cd_TOC.md)

![beginning](md_Graphics/start_sm.jpg)

## **IML** stands for Integrated Manager for Lustre.

## **IML** is responsible for the installation, configuration, monitoring, and overall management of [Lustre](http://lustre.org/).

The Lustre file system is an open-source, parallel file system, generally used for large-scale cluster computing.

## Below are some screen shots of **IML:**

### Login Screen

![iml_login.png](md_Graphics/iml_login.png)

### Server Screen

![iml_spa.png](md_Graphics/iml_spa.png)

- More [IML Screenshots](cd_Screen_Shots.md)

## Source Code

Before accessing our source code repository for the first time, new contributors should have a good understanding of the tools and processes in place.

- Become very familiar with [git](https://git-scm.com/docs).
- Become familiar with the [IML codebase](https://github.com/whamcloud).
- Learn the [IML contributor workflow](cd_Contributor_Workflow.md).
- Understand How to Contribute to the [Frontend](cd_Contribute_To_Frontend.md) and/or [Backend](cd_Contribute_To_Backend.md) Code.
- Be ready to learn new things.

## Frontend Code and Backend Code

IML consists of a **Frontend GUI** that is written primarily in **Node JS** and server-side **Backend** code that is written primarily in **python**. The codebase relies on many external dependencies and uses many services and APIs.

![iml_flow](md_Graphics/2017_0803_backend_frontend.png)

The [IML codebase](https://github.com/whamcloud) consists of many repositories due to the varying needs and varying dependencies.

## Primary IML repos

| Repo Name                                                                                       | Description                                                                                                                          |
| ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| [integrated-manager-for-lustre](https://github.com/whamcloud/integrated-manager-for-lustre)     | Consider this as the _Top level_ repo populated mostly with python code.                                                             |
| [GUI](https://github.com/whamcloud/GUI)                                                         | The Graphical User Interface for the Single Page Application, IML. This is primarily nodejs code with angular and inferno libraries. |
| [manager-for-lustre-dependencies](https://github.com/whamcloud/manager-for-lustre-dependencies) | Dependencies needed for IML that are not available elsewhere.                                                                        |
| [view-server](https://github.com/whamcloud/view-server)                                         | Server client-side files.                                                                                                            |
| [socket-worker](https://github.com/whamcloud/socket-worker)                                     | Off main thread data munging.                                                                                                        |
| [realtime](https://github.com/whamcloud/realtime)                                               | WebSocket Proxy over RESTful API.                                                                                                    |
| [Vagrantfiles](https://github.com/whamcloud/Vagrantfiles)                                       | Configuration used to generate a virtual lustre clustre with vagrant and virtualBox.                                                 |

## Dependencies for IML

### High level python dependencies

- The [django](https://www.djangoproject.com/) web application framework.
- [Tastypie](https://django-tastypie.readthedocs.io/en/latest/) webservice API framework for Django used as the REST-api.
- [django-south](https://south.readthedocs.io/en/latest/), a tool to provide consistent, easy-to-use and database-agnostic migrations for Django applications.
- [Kombu](https://pypi.python.org/pypi/kombu) messaging library for python.
- [Supervisor](http://supervisord.org/), a system for controlling process state under linux.
- **Robinhood**

## IML Services

### IML uses the following services

| Service Name | Description                                                                                                   |
| ------------ | ------------------------------------------------------------------------------------------------------------- |
| corosync     | A group communication system with additional features for implementing high availability within applications. |
| gunicorn     | 'Green Unicorn' is a Python WSGI HTTP Server for UNIX.                                                        |
| http_agent   | Communicates with the agent daemon on storage servers.                                                        |
|              |                                                                                                               |

## Other Services:

- job_scheduler
- lustre_audit
- plugin_runner
- power_control
- realtime
- stats
- syslog
- view_server

---

[Top of page](#introduction)
