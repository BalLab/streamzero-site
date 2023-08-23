---
title: "Containers + Purpose"
linkTitle: "Containers & Purpose"
weight: 5
description: >
  StreamZero SX Containers + Purpose.
---

## Creating a Docker Container

Below is an example of a dockerfile to create a Docker image for some StreamZero SX application. The user is free to choose what base python image
to use and then add StreamZero module and other libraries.

```
FROM python:3.9-alpine
#RUN pip install -i https://test.pypi.org/simple/ StreamZero-sx==0.0.8 --extra-index-url https://pypi.org/simple/ StreamZero-sx
RUN pip install StreamZero-sx
COPY app.py utils.py
```

After the user have built an image and pushed it to some Docker image regitry, he can run it in StreamZero SX UI.
