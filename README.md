## ssh into a vagrant box

[ssh into a vagrant box instructions](http://www.hashbangcode.com/blog/connecting-vagrant-box-without-vagrant-ssh-command)

In order to use an alias to ssh into a vagrant box we need to set up the config
file in `.ssh/config`

In this case we're aliasing the vagrant box as econ-local. The config file is
include in the repo as an example.

## Move the git deployment ssh key onto vagrant
we're gonig to automatically pull down repos from github. In order to pull down
repos from github we need to put the deployment keys onto the vagrant box. Use 
scp to move the deployment key onto the vagrant box. Once the key is on the vagrant
box, ssh into the box and move the key to `/home/econ/.ssh`. The deployment
key location (on the vagrant box) is specified in [the linked playbook] (https://github.com/economicAnalysis/econ-ansible/blob/master/playbooks/app-db/deploy-build-db.yml)