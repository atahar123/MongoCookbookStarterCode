# Mongo DB Cookbook

This cookbok installs mongodb from source.
It creates its own apt package and then installs it.
The recipe also creates the config files and the service file with dynamic input of variables.

## List of what installs
- Mongodb

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
