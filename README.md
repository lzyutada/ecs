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
## make container permanent
1. 使用基础镜像
'''FROM ubuntu:24.04'''
2. 设置工作目录
'''WORKDIR /app'''
3. 安装系统依赖 (一次性搞定)
'''RUN apt update && apt install -y python3 python3-pip'''
4. 安装 Python 依赖
'''RUN pip3 install flask gunicorn --break-system-packages'''
5. 容器启动时默认执行的命令
'''CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:5000", "app:app"]'''
