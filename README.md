# CgloW-OnlineJudge

Make sure 'docker.io', 'rabbitmq-server' is installed.

make sure rabbitmq-server is listening to port 5672

language python3

installation -- >

'pip3 install virtualenv'

'python3 -m virtualenv projectCglow'

'cd projectCglow/'

'source bin/activate'

'git clone https://github.com/TariqueNasrullah/cglow.git'

'pip install django'

'pip install celery'

'pip install docker'


Goto 'projectCglow/cglow/contestjudger' and RUN 

'docker build -t contestjudger .'  -don't forget the (.) dot.

Goto 'projectCglow/cglow/offlinejudger' and RUN 

'docker build -t offlinejudger .'  -don't forget the (.) dot.

Goto 'projectCgloW/cglow' and RUN 

'python manage.py runserver'

On another terminal, goto 'projectCglow/' and RUN
 
'source bin/activate'

'cd cglow'

'celery -A cglow worker -l info'


On your browser locate to http://127.0.0.1:8000
