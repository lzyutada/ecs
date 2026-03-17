# ecs
Elastic Compute Service

# ubuntu + docker
1. install docker in host
2. create docker container and bind with host port
  -  mount path in host
  -  bind host port with container port
4. exec docker container
5. installing python3, python3-pip, flask, gunicorn in container
6. Testing:
  - runing gunicorn with reloaded
  - visit page provided by container
  - change page content
  - refresh from webbrowser
