# codbex-documentation

## Build

### Python

Install Python using OS dependent packager https://www.python.org/downloads/

Install MkDocks

```
pip3 install mkdocs
```

Start a local server

```
python3 -m mkdocs serv
```

### Docker

```
docker pull squidfunk/mkdocs-material:latest
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material:latest
```

Go to http://localhost:8000 to access the site content.
