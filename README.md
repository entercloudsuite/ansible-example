ansible-example 
======================================

[![Build Status](https://travis-ci.org/entercloudsuite/ansible-example.svg?branch=master)](https://travis-ci.org/entercloudsuite/ansible-example)
[![Galaxy](https://img.shields.io/badge/galaxy-entercloudsuite.example-blue.svg?style=flat-square)](https://galaxy.ansible.com/entercloudsuite/example)

Example playbook to use as an implementation reference.

# usage
1. Run `molecule create` to start the target Docker container on your local engine.  
2. Use `molecule login` to log in to the running container.  
3. Edit the role files.  
4. Add other required roles (external) in the molecule/default/requirements.yml file.  
5. Edit the molecule/default/playbook.yml file to list the roles to run.  
6. Define infra tests under the molecule/default/tests folder using the goos verifier.  
7. When ready, use `molecule converge` to run the Ansible Playbook and `molecule verify` to execute the test suite.  
Note that the converge process starts performing a syntax check of the role.  
Destroy the Docker container with the command `molecule destroy`.   

To run all the steps with just one command, run `molecule test`.  
