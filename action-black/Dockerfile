FROM python:3.6.8-alpine

LABEL "name"="Python Action Black"
LABEL "homepage"="https://github.com/jefftriplett/python-actions"
LABEL "maintainer"="Jeff Triplett <jeff.triplett@users.noreply.github.com>"
LABEL "repository"="https://github.com/jefftriplett/python-actions"
LABEL "version"="1.0.0"

LABEL "com.github.actions.name"="Python Action Black"
LABEL "com.github.actions.description"="Lint your Python code with Black"
LABEL "com.github.actions.icon"="mic"
LABEL "com.github.actions.color"="blue"

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

COPY requirements.txt /requirements.txt

RUN pip install --no-cache-dir \
        -r /requirements.txt && \
    rm -rf /root/.cache/

COPY entrypoint.sh /entrypoint.sh

WORKDIR /workspace

ENTRYPOINT [ "/entrypoint.sh" ]
CMD [ "--help" ]
