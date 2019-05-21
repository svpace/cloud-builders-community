FROM python:3-alpine

RUN \
    apk --update add --virtual build-dependencies python-dev libffi-dev openssl-dev build-base && \
    pip install --no-cache-dir ansible && \
    apk del build-dependencies && \
    rm -rf /var/cache/apk/*

ENTRYPOINT ["/usr/bin/ansible-playbook"]
