# play-ansible
## Setup

##### 1. Create the deploy user (this must be done on every host)

1. ssh into the server via root account
2. Add the deploy user `adduser deploy`
3. Add user to the sudo group `adduser deploy sudo` (optional)
4. Exit the server `exit`

##### 2. Ansibilize the hosts

Ansible is used to provision and setup the hosts for the application. 

```ruby
me@localhost: ansible-playbook -i staging ansibilize.yml -c paramiko --ask-sudo-pass
```
