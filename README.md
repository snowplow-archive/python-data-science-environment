# Python Data Science environment

VM with complete R (RStudio) environment. Setup an R environment without any faff.

## Quickstart

Assuming git, [Vagrant] [vagrant-install] and [VirtualBox] [virtualbox-install] installed:

```
 host$ git clone https://github.com/snowplow/python-data-science-environment.git
 host$ cd python-data-science-environment
 host$ vagrant up
```

This will launch a VM, install on it Python on it including all the libraries commonly associated with doing data-science with Python. You then simply need to ssh on:

```
host$ vagrant ssh
```

Start ipython

```
guest$ /home/vagrant/python-data-science/bin/ipython notebook --ip=0.0.0.0 --no-browser
```

And then navigate to `http://localhost:8888` on the host

Simple!


## Notes

Data-science requires lots of RAM - this VM has been built on the basis it is run on a host with 16GB of RAM. (It takes 10GB for the VM.)

To adjust the amount of RAM used, update the following line in the `Vagrantfile` prior to executing `vagrant up`:

```bash
    vb.memory = 10240
```

[vagrant-install]: http://docs.vagrantup.com/v2/installation/index.html
[virtualbox-install]: https://www.virtualbox.org/wiki/Downloads
