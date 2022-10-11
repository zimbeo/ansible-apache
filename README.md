# ansible-apache
In order to run this ansible playbook, run the below command on a control node that has SSH access to your host you are setting up. 

```ansible-playbook -i hosts site.yml --ask-become-pass```

## What does this run on?
In my ``hosts`` file I define the below which basically says - 
I have a group of hosts (in the example, only one) named webservers which contains the server with the hostname of, ``home-ubuntu-01``. 
```
[webservers]
home-ubuntu-01
```
This is referenced in the ``site.yml`` file which basically is the brains of the entire playbook. The ``site.yml`` defines which host groups things should run on, who the playbook should log in as (henry in this case), and what roles it should setup - just ``web`` in this case.
