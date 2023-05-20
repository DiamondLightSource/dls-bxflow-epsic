Installing
=======================================================================


You will need python ${python_version_at_least} or later. 

On a Diamond Light Source internal computer, you can achieve Python ${python_version_at_least} by::

    $ module load python/${python_version_at_least}

You can check your version of python by typing into a terminal::

    $ python3 --version

It is recommended that you install into a virtual environment so this
installation will not interfere with any existing Python software::

    $ python3 -m venv /scratch/$USER/myvenv
    $ source /scratch/$USER/myvenv/bin/activate
    $ pip install --upgrade pip


You can now use ``pip`` to install the library and its dependencies::

    .. ifconfig:: pip_find_links

        $ export PIP_FIND_LINKS=${pip_find_links}

    $ python3 -m pip install ${repository_name}

If you require a feature that is not currently released you can also install
from git::

    $ python3 -m pip install git+${git_url}/${repository_name}.git

The library should now be installed and the commandline interface on your path.
You can check the version that has been installed by typing::

    $ ${repository_name} --version
    $ ${repository_name} --version-json
