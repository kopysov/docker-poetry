FROM python:3.9-slim

ENV POETRY_VERSION=1.1.7 \
    POETRY_HOME=/opt/poetry
ENV PATH=$POETRY_HOME/bin:$PATH

RUN set -ex \
	&& python -m venv --clear $POETRY_HOME/venv \
	&& $POETRY_HOME/venv/bin/python -m pip --no-cache-dir install poetry==$POETRY_VERSION \
	&& mkdir $POETRY_HOME/bin \
	&& ln -s $POETRY_HOME/venv/bin/poetry $POETRY_HOME/bin/ \
	&& poetry config virtualenvs.path $POETRY_HOME/virtualenvs
