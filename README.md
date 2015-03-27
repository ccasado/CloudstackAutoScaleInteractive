CloudStack Auto Scale Interactive
=================================

Python interactive script to perform autoscale functions with Apache Cloudstack API.

Using Python client library for the CloudStack User API v3.0.0. For older versions,
see the https://github.com/jasonhancock/cloudstack-python-client/tags.

Script Setup
--------

You need to create the properties file to setup script with parameters to access cloudstack api and to define zone to auto scale

```
$ touch properties
```

Edit the properties file with the contents below:

```
[ConfigApi]
api: https://host:443/client/api
apikey: xxxxxx
secret: xxxxxx

[Envs]
zoneid: xxxxxx
```

Executing Script
--------

```
$ python CloudstackAutoScale.py -h
usage: CloudstackAutoScale.py [-h] -c COMMAND -o OPTION

Cloudstack Auto Scale script.

optional arguments:
  -h, --help            show this help message and exit
  -c COMMAND, --command COMMAND
                        counter, condition, policy, vmprofile or vmgroup
  -o OPTION, --option OPTION
                        list or create
```

TODO
--------
- [X] Display template name and serviceoffering name in vmprofile list function;
- [ ] Function to list autoscale vm group;
- [ ] Function to create counters;
- [ ] Function to list load balancers rules;
- [ ] Remove to all commands;
- [ ] Validate all inputs;
- [ ] Enable to create an autoscale in projects


References
--------
* https://github.com/jasonhancock/cloudstack-python-client

