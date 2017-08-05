Welcome to zunzunsite, a Django site in Python 2 for curve fitting 2D
and 3D data that can output source code in several computing languages
and run a genetic algorithm for initial parameter estimation. Includes
orthogonal distance and relative error regressions. Generates PDF files
and surface animations. Based on code from zunzun.com. 

You will need to install scipy, matplotlib, django, beautifulsoup,
imagemagick, gifsicle, reportlab to run this software.

On Debian and Ubuntu, you can run:

apt-get install python-scipy python-matplotlib
apt-get install python-django python-beautifulsoup
apt-get install python-reportlab python-reportlab-accel
apt-get install imagemagick gifsicle


then install the pyeq2 fitting code with these commands:

apt-get install python-pip
pip install pyeq2


You can now cd to the project's top-level directory and
run the django development server with the command:

python manage.py runserver

and open the url http://127.0.0.1:8000/ in a browser. Cool!


NOTES: the code uses Unix-style process forking, and this
is not available on the  Windows operating system.

My tests show that while both mod_wsgi and gunicorn work fine
for Django production servers, the uwsgi process model would not
allow os.fork() calls to work as required for this software.
