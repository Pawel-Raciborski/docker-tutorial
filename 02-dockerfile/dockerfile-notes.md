# What is Dockerfile

It's a text document that contains all commands a user could call on the command line to assemble an image. It's used to create container image.

Every container created based on image got filesystem.

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

If we are using instruction **RUN** to run some instrucions by default they will be executed in **root file**

[Instructions available in Dockerfile](https://docs.docker.com/reference/dockerfile/#overview)


Conventions:
- Instructions write UPPERCASE