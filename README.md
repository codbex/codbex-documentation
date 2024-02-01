# codbex-documentation

## Build

### Python

```
python3 -m mkdocs serv
```

### Docker

```
docker pull squidfunk/mkdocs-material:latest
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material:latest
```

Go to http://localhost:8000 to access the site content.