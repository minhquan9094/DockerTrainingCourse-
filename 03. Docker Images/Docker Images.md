# Docker Images



### Lab01: Build docker image with FLASK


#### Step to create image

1. import OS
2. Update repo
3. Install Dependencies
4. install python lib/dependencies
5. Copy source to docker folder
6. Run webserver

#### Sourcecode app.py


```
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "<p>Hello, World!</p>"

```

#### Dockerfile
```
FROM Ubuntu

RUN apt-get update
RUN apt-get install python3
RUN apt-get install python3-pip

RUN pip install flask
RUN pip instlal flask-mysql

COPY app.py /opt/source-code/app.py

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask run

```

