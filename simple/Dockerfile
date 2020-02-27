FROM python:alpine
RUN pip install \
        mkdocs==1.1 \
        mkdocs-material==4.6.3
EXPOSE 8000
WORKDIR /docs
CMD ["mkdocs", "serve", "--dev-addr=0.0.0.0:8000"]
