---
title: "airflow setting error & solution"
tag: 
    - airflow 
    - data
---
- Error : By default one of Airflow's dependencies installs a GPL 

- Error Detail : RuntimeError: By default one of Airflow's dependencies installs a GPL dependency (unidecode). To avoid this dependency set SLUGIFY_USES_TEXT_UNIDECODE=yes in your environment when you install or upgrade Airflow. To force installing the GPL version set AIRFLOW_GPL_UNIDECODE 
Command "python setup.py egg_info" failed with error code 1 in /tmp/pip-build-6CXkiw/apache-airflow

- environment : ubuntu-18.04.1

- Solution : sudo SLUGIFY_USES_UNIDECODE=yes pip install apache-airflow 
