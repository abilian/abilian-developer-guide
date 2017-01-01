Devops
======

(Very scketchy for now).

Principles
----------

- <https://12factor.net/> 
- <http://www.clearlytech.com/2014/01/04/12-factor-apps-plain-english/>

Note: we're not yet 12 factor compatible, actually, due to our reliance on local
file storage. This will probably be fixed in 2017.

- <https://zachholman.com/posts/deploying-software>

Tools
-----

- Fabric
- Invoke <https://github.com/pyinvoke/invoke>
- Docker
- Vagrant (for dev, not prod)

+ to investogate:

- <http://platter.pocoo.org/dev/>
- <http://pythonhosted.org/fapistrano/>


Platforms
---------

- Heroku (for playing purposes)
- Dokku (open source Heroku alternative, 
- Kubernetes
- Or plain old "a la mano" deployment (using Fabric, Invoke...) using nginx as a front-end web server and either gunicorn (currently preferred) or uwsgi as application server, with supervisord for process management.

Monitoring, etc.
----------------

- Sentry / getsentry
- <http://uptimerobot.com/>


