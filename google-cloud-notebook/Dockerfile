# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.
FROM jupyter/tensorflow-notebook

MAINTAINER Steven Hancock <shancock@vendasta.com>

USER $NB_USER

# Added --ignore-installed. See https://stackoverflow.com/questions/42020151/cannot-remove-entries-from-nonexistent-file
RUN pip install --upgrade setuptools --ignore-installed

# Install google stuff
RUN pip install 'google-api-python-client'

RUN pip install 'google-cloud'
RUN pip install 'google-cloud-bigquery'

RUN pip install --upgrade google-cloud
RUN pip install --upgrade google-cloud-bigquery
RUN pip install --upgrade oauth2client

RUN pip install 'pandas-gbq'

# Set google application environment variable so we can login without issue
ENV GOOGLE_APPLICATION_CREDENTIALS=/home/jovyan/work/VendastaBizOps-key.json
