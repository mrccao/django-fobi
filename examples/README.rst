============================================
Example project for `django-fobi`
============================================
Follow instructions below to install the example project. Commands below are written for Ubuntu/Debian,
but may work on other Linux distributions as well.

- Create a new- or switch to existing- virtual environement.

    $ virtualenv fobi

    $ source fobi/bin/activate

- Download the latest stable version of django-fobi.

    $ wget https://github.com/barseghyanartur/django-fobi/archive/stable.tar.gz

- Unpack it somewhere.

    $ tar -xvf stable.tar.gz

- Go to the unpacked directory.

    $ cd django-fobi-stable

- Install Django, requirements and finally django-fobi.

    $ pip install Django

    $ pip install -r example/requirements.txt

    $ pip install -e git+https://github.com/barseghyanartur/django-fobi@stable#egg=django-fobi

- Create some directories.

    $ mkdir -p examples/media/static/ examples/static/ examples/db/ examples/logs

- Copy local_settings.example

    $ cp examples/simple/local_settings.example examples/simple/local_settings.py

- Run the commands to sync database, install test data and run the server.

    $ python examples/example/manage.py syncdb --noinput --traceback -v 3

    $ python examples/example/manage.py migrate --noinput

    $ python examples/example/manage.py collectstatic --noinput --traceback -v 3

    $ python examples/example/manage.py fobi_create_test_data --traceback -v 3

    $ python example/example/manage.py runserver 0.0.0.0:8001 --traceback -v 3

- Open your browser and test the app.

Fobi interface:

- URL: http://127.0.0.1:8001/forms/builder/
- Admin username: test_admin
- Admin password: test

Django admin interface:

- URL: http://127.0.0.1:8001/admin/
- Admin username: test_admin
- Admin password: test

Various setups
============================================
There are number of setups included (names are self-explanatory):

- Bootstrap3 theme + Captcha (runserver-bootstrap3-theme-captcha) :8000
- Bootstrap3 theme + Django 1.7 + Captcha (runserver-bootstrap3-theme-django17-captcha) :8000
- Bootstrap3 theme + Django 1.7 (runserver-bootstrap3-theme-django17) :8000
- Bootstrap3 theme + FeinCMS integration (runserver-bootstrap3-theme-feincms-integration) :8000
- Bootstrap3 theme (runserver-bootstrap3-theme) :8000

- Foundation 5 theme + FeinCMS integration (runserver-foundation5-theme-feincms-integration) :8001
- Foundation 5 theme :8001

- Override of the simple theme (runserver-override-simple-theme) :8003

- Simple theme (runserver-simple-theme) :8002
