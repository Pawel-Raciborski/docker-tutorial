# What is Dockerfile

It's a text document that contains all commands a user could call on the command line to assemble an image. It's used to create container image.


### Dockerfile format:

```dockerfile
#Comment
INSTRUCTION args
```

### Example of Dockerfile:
```dockerfile
FROM python:3.12
WORKDIR /usr/local/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY src ./src
EXPOSE 5000

RUN useradd app
USER app

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8080"]
```

[Instructions available in Dockerfile](https://docs.docker.com/reference/dockerfile/#overview)


Conventions:
- Instructions write UPPERCASE