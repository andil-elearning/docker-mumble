# docker-mumble

After building and starting the containers, things will not work by themselves.
Some processes cannot be automated ; there's one script that cannot be executed without an interface.

So you will have to :

- get into the "mumble-web" container (you can check its name with `docker ps`)
- execute `/usr/share/mumble-django/pyweb/manage.py syncdb`
- copy the line that starts with `Meta:` and change the ip adress with `head`
- Create the super user

There can be a warning, but it will still work.
