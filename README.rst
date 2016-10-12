pipsi
=====

This is a fork of `mitsuhiko/pipsi`_.

.. _`mitsuhiko/pipsi`: https://github.com/mitsuhiko/pipsi

The change has been made for my use of `conda` instead of `virtualenv`.

Boostrapping and Installation::

      cd $HOME
      conda create -p ~/.local/venvs/pipsi --no-default-packages pip
      ./.local/venvs/pipsi/bin/pip install git+https://www.github.com/feigaoxyz/pipsi.git
      ln -s ~/.local/venvs/pipsi/bin/pipsi ~/.local/bin/pipsi


You can read the original README below for usage.

---------------------

pipsi = pip script installer

What does it do?  pipsi is a wrapper around virtualenv and pip
which installs scripts provided by python packages into separate
virtualenvs to shield them from your system and each other.

In other words: you can use pipsi to install things like
pygmentize without making your system painful.

How do I get it?

::

    curl https://raw.githubusercontent.com/mitsuhiko/pipsi/master/get-pipsi.py | python

How does it work?

pipsi installs each package into ~/.local/venvs/PKGNAME and then
symlinks all new scripts into ~/.local/bin.

Installing scripts from a package::

      $ pipsi install Pygments

Uninstalling packages and their scripts::

      $ pipsi uninstall Pygments

Upgrading a package::

      $ pipsi upgrade Pygments

Showing what's installed::

      $ pipsi list

How do I get rid of pipsi?

::

      $ pipsi uninstall pipsi

How do I upgrade pipsi?  With 0.5 and later just do this::

      $ pipsi upgrade pipsi

On older versions just uninstall and reinstall.
