FROM public.ecr.aws/docker/library/python:3.12.7-slim-bookworm
COPY workspaces_app /workspaces_app

WORKDIR /workspaces_app
RUN adduser -uid 1001 nonroot
USER nonroot

RUN pip install -r ./setup_requirements.txt
RUN pip install -r ./requirements.txt
CMD python3 ./main.py
