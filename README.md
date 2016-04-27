ansible-ruby-2.3.0
=========

Installs Ruby-2.3.0 compiling from source. All the binaries have symbolic links at /usr/local/ruby-2.3.0.

Requirements
------------

None.

Role Variables
--------------

`ruby_230_dir` 
The final destination of Ruby files, default is `/usr/local/ruby-2.3.0`.


`ruby_230_compile_options` 
Ruby compile options, default is `--prefix={{ ruby-230_dir }} --disable-install-rdoc && make && make install`.


Dependencies
------------

None.

Example Playbook
----------------

This role comes with a Vagrant file. Just fire a `vagrant up` for testing.     
Once the environemnt is up, just run `vagrant provision` or `ansible-playbook -i tests/inventory tests/test.yml`.     
As the date of this commit, the parameter `host_key_checking=False` it's not working. If some SSH connection error occurs, try to execute `export ANSIBLE_HOST_KEY_CHECKING=False`.    

In production, is really simple to use, you can run as:

```
  - hosts: servers
    roles:
    - { role: jonatasbaldin.ruby-2.3.0 }
```

License
-------

MIT License.

Author Information
------------------

Jonatas Baldin      
<mailto:jonatas.baldin@gmail.com>      
http://deployeveryday.com
