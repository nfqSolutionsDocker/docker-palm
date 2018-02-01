### python CONTENEDOR PARA PALM

This container has the following characteristics:

- Python 3.4 installed.
- Pip 3.4 installed.
- Volumen is /solutions/app.

Create into volumen '/solutions/app' the 'rpm' folder to put the rpm files to install in start container.
Important, add in rpm files name the numbers order to install.

Create into volumen '/solutions/app' the 'pip' folder to put the zip files to install in start container.
Important, add in zip files name the numbers order to install.

Add in docker-compose file 'PIP_PACKAGES' variable to install with pip 3.4 in start container.
Add in docker-compose file 'PYTHON_FILES' variable to execute with python 3.4 in start container.

For example, docker-compose.yml:
```
app:
 image: nfqsolutions/palm
 restart: always
 environment:
  - PACKAGES=
  - PIP_PACKAGES=
  - PYTHON_FILES=
  - SERVICES=
 ports:
  - "8080:8888"
 volumes:
  - <mydirectory>:/solutions/app
  - <mydirectory>/pip:/solutions/app/pip
  - <mydirectory>/apps/rpm:/solutions/app/rpm
 
```


