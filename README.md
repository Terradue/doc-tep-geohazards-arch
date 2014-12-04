## Geohazards Thematic Exploitation Platform Architecture

[![Build Status](https://build.terradue.com/buildStatus/icon?job=tep.doc-tep-geohazards-arch)](https://build.terradue.com/job/tep.doc-tep-geohazards-arch/)

This is the official repository of the Tep QuickWin Architecture. 

This documentation is live at:
[http://terradue.github.io/doc-tep-geohazards-arch](http://terradue.github.io/doc-tep-geohazards-arch)

You are encouraged to fork this repo and send us pull requests!

### Getting started

Here's the procedure to install the required packages on a CentOS 6.x

```
# Install RHEL EPEL repository
$ wget http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
$ wget http://rpms.famillecollet.com/enterprise/remi-release-6.rpm
$ sudo rpm -Uvh remi-release-6*.rpm epel-release-6*.rpm

# Install sphinx
$ sudo yum install python-sphinx10
$ sudo yum install python-pip
$ sudo pip install sphinx_bootstrap_theme
$ sudo ln -s /usr/bin/sphinx-1.0-build /usr/bin/sphinx-build
```

**Patch:** Open the file */usr/lib/python2.6/site-packages/sphinx_bootstrap_theme/bootstrap/globaltoc.html* and substitute:

```
maxdepth=theme_globaltoc_depth|toint
```

with:

```
maxdepth=theme_globaltoc_depth
```

```bash
# Install plantuml
$ wget --no-check-certificate https://pypi.python.org/packages/source/s/sphinxcontrib-plantuml/sphinxcontrib-plantuml-0.3.tar.gz
$ tar xvzf sphinxcontrib-plantuml-0.3.tar.gz 
$ cd sphinxcontrib-plantuml-0.3
$ sudo pip install sphinxcontrib-plantuml
$ cat << EOF > /usr/bin/plantuml
#!/bin/sh -e
java -jar /usr/lib/plantuml.7997.jar "$@"
EOF
$ chmod +x /usr/bin/plantuml

# Clone the git repository
$ git clone git@github.com:Terradue/doc-developer-sandbox.git
```

If needed, set your github information:

```bash
$ git config --global user.name <github username>
$ git config --global user.email <email address>
```

### Building

Build the documentation by running ``make html``.


### Publish the documentation

``make html`` creates a ``build`` folder in the doc-developer-sandbox local repository.

As root, do:

```
$ sudo cd /var/www/html
$ ln -s $GIT_CLONE_DIR/doc-tep-geohazards-arch/build/html/ doc-tep-geohazards-arch
$ chown -R apache:apache doc-tep-geohazards-arch
$ chmod -R g+w doc-tep-geohazards-arch
```
> Replace $GIT_CLONE_DIR with the path to the folder where you have cloned the repository

Open you browser at the address http://127.0.0.1/doc-tep-geohazards-arch

#### This documentation is built with [sphinx](http://sphinx-doc.org/).
