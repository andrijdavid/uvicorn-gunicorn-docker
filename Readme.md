# uvicorn-gunicorn

[**Docker**](https://www.docker.com/) image with [**Uvicorn**](https://www.uvicorn.org/) managed by [**Gunicorn**](https://gunicorn.org/) for high-performance web applications in **[Pypy](https://www.pypy.org/) with performance auto-tuning.

**GitHub repo**: <https://github.com/andrijdavid/uvicorn-gunicorn-docker>

**Docker Hub image**: <https://hub.docker.com/r/andrijdavid/uvicorn-gunicorn/>


## Description

Python web applications running with **Uvicorn** (using the "ASGI" specification for Python asynchronous web applications) have shown to have [some of the best performances, as measured by third-party benchmarks](https://www.techempower.com/benchmarks/#section=test&runid=a979de55-980d-4721-a46f-77298b3f3923&hw=ph&test=fortune&l=zijzen-7).

The achievable performance is on par with (and in many cases superior to) **Go** and **Node.js** frameworks.

This image has an "auto-tuning" mechanism included, so that you can just add your code and get that same **high performance** automatically. And without making sacrifices.


## Technical Details


### Uvicorn

**Uvicorn** is a lightning-fast "ASGI" server.

It runs asynchronous Python web code in a single process.


### Gunicorn

You can use **Gunicorn** to manage Uvicorn and run multiple of these concurrent processes.

That way, you get the best of concurrency and parallelism.


### `tiangolo/uvicorn-gunicorn`

This image will set a sensible configuration based on the server it is running on (the amount of CPU cores available) without making sacrifices.

It has sensible defaults, but you can configure it with environment variables or override the configuration files.



## Description

Python web applications running with **Uvicorn** (using the "ASGI" specification for Python asynchronous web applications) have shown to have [some of the best performances, as measured by third-party benchmarks](https://www.techempower.com/benchmarks/#section=test&runid=a979de55-980d-4721-a46f-77298b3f3923&hw=ph&test=fortune&l=zijzen-7).

The achievable performance is on par with (and in many cases superior to) **Go** and **Node.js** frameworks.

This image has an "auto-tuning" mechanism included, so that you can just add your code and get that same **high performance** automatically. And without making sacrifices.


## Technical Details


### Uvicorn

**Uvicorn** is a lightning-fast "ASGI" server.

It runs asynchronous Python web code in a single process.


### Gunicorn

You can use **Gunicorn** to manage Uvicorn and run multiple of these concurrent processes.

That way, you get the best of concurrency and parallelism.


### `andrijdavid/uvicorn-gunicorn`

This image will set a sensible configuration based on the server it is running on (the amount of CPU cores available) without making sacrifices.

It has sensible defaults, but you can configure it with environment variables or override the configuration files.


# Credit

https://github.com/tiangolo/uvicorn-gunicorn-docker/


