# ansible_infra

Is a collection of useful ansible scripts I encountered and used.

*Rough Structure*
```
 |-> ansible_infra
      |-> ansible.cfg
      |-> core/
           |-> roles/
                 |-> ansible-role-jenkins -> ../roles/geerlingguy.jenkins
                 ...
                 |-> ansible-role-java    -> ../roles/geerlingguy.java
           |-> .roles
                 |-> geerlingguy.jenkins
                 ...
                 |-> geerlingguy.java
                 |-> roles.txt
```

*Follow a Role*

1. cd ansible_infra/core/.roles
2. git submodule add https://github.com/geerlingguy/ansible-role-mysql geerlingguy.mysql
3. ln -s ./geerlingguy.mysql ../roles/ansible-role-mysql
4. Update roles/roles.txt

*Updating Followed Role*
1. git clone https://github.com/icasimpan/ansible-roles.git
2. cd ansible-roles/roles
3. git submodule init
4. git submodule update
