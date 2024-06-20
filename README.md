# data-sharing-platform


Create a Python virtual environment and activate it:

    sudo mkdir -p /usr/lib/ckan/default
    sudo chown `whoami` /usr/lib/ckan/default
    python3 -m venv /usr/lib/ckan/default
    . /usr/lib/ckan/default/bin/activate

Install the recommended setuptools version and up-to-date pip:

     pip install --upgrade pip

Install the CKAN source code into your virtualenv.

To install the latest stable release of CKAN (CKAN 2.10.1), run:

    pip install -e 'git+https://github.com/ckan/ckan.git@ckan-2.10.1#egg=ckan[requirements]'

Deactivate and reactivate your virtualenv, to make sure you’re using the virtualenv’s copies of commands like ckan rather than any system-wide installed copies:

    deactivate
    . /usr/lib/ckan/default/bin/activate

Running DSP

    python3 -m venv /usr/lib/ckan/default
    . /usr/lib/ckan/default/bin/activate
    cd /usr/lib/ckan/default/src/ckan
    sudo ckan -c /etc/ckan/default/ckan.ini run


/--------------------------installing datapusher-----------------/

    sudo apt-get install python-dev python-virtualenv build-essential libxslt1-dev libxml2-dev zlib1g-dev git libffi-dev
    
    git clone https://github.com/ckan/datapusher
    cd datapusher
    
    pip install -r requirements.txt
    pip install -r requirements-dev.txt
    pip install -e .
    
    pip install SQLAlchemy==1.4.0

/---------------------------running / repairing datapusher-------------------/

    pip install -U urllib3 requests
    cd datapusher
    python datapusher/main.py deployment/datapusher_settings.py
