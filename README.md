# Mongo DB Cookbook

This cookbok installs mongodb from source.
It creates its own apt package and then installs it.
The recipe also creates the config files and the service file with dynamic input of variables.

## List of what installs
- Mongodb

## Prerequisites
- Chef
### What is Chef?
- Chef is a configuration management tool which allows you to provision files for installation.
- It allows you to be infrastructure agnostic.
- Chef allows for machines to be setup on physical machines, in the cloud and virtual machines.

## Clone
```
git clone git@github.com:atahar123/MongoCookbookStarterCode.git
```

## Options and setting variables
Please go to attributes folder and change what you need to change.

Change the port:
```
# attributes/default.rb
default['mongo']['port'] = <new_value_here>
```

## Commands

### Test locally
Running my unit test:
```
chef exec rspec
```

Running Integration tests and closing VM:
```
kitchen test
```

### Test in AWS
Running Integration tests in AWS
```
KITCHEN_YAML=yml_file_name.yml kitchen test
```
