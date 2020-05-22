# iter8-analytics

[![Build Status](https://travis-ci.com/iter8-tools/iter8-analytics.svg?branch=master)](https://travis-ci.com/iter8-tools/iter8-analytics)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

This is the repo for the `iter8-analytics` component of `iter8`. For all `iter8` documentation, please, refer to [https://github.com/iter8-tools/docs](https://github.com/iter8-tools/docs).

## Running iter8-analytics v1.0.0 locally
The following instructions have been tested in a Python 3.7.4 virtual environment.

```
1. git clone git@github.com:iter8-tools/iter8-analytics.git
2. cd iter8-analytics
3. pip install -r requirements.txt 
4. export ITER8_ANALYTICS_METRICS_BACKEND_URL=<URL of your prometheus service>
5. cd iter8-analytics
6. python fastapi_app.py 
```
Navigate to http://localhost:5555/docs on your browser. You can interact with the iter8-analytics service and read its API documentation here. When you `POST` requests to iter8-analytics, it interacts with Prometheus -- make sure your Prometheus URL in step 4 is accessible if you want this interaction to work.

## Testing iter8-analytics v1.0.0 locally
The following instructions have been tested in a Python 3.7.4 virtual environment.

```
1. git clone git@github.com:iter8-tools/iter8-analytics.git
2. cd iter8-analytics
3. pip install -r requirements.txt 
4. pip install -r test-requirements.txt 
5. export ITER8_ANALYTICS_METRICS_BACKEND_URL=<URL of your prometheus service>
6. make test
```
You can see the coverage report by opening `htmlcov/index.html` on your browser. The prometheus URL in step 5 is a dummy URL since all Prometheus calls are mocked in tests.
