Your own OSQA on OpenShift
============================

This git repository helps you get up and running quickly w/ a Django installation on OpenShift.  The Django project name used in this repo is 'osqa' but feel free to change it. 

Create the app on OpenShift
----------------------------

Create an account at http://openshift.redhat.com/ , don't forget to create a namespace and install client tools as well.

Create a python application

    rhc app create -a osqa -t python-2.6

Add mysql database support for you app

    rhc app cartridge add -a osqa -c mysql-5.1

Grab this quickstart codes and make it working for you!

    cd osqa
    git remote add upstream -m master git://github.com/openshift/OSQA-openshift-quickstart.git
    git pull -s recursive -X theirs upstream master
    git push

That's it, you can now checkout your application at:

    http://osqa-$yournamespace.rhcloud.com
