## setup

## ssh for headless

Create file named ```ssh```  within the boot partition of the sd card.

```
username: pi
password: raspberry
```

Then connect via ```ssh pi@192.168.1.42``` (adjust the IP)


further reading

* https://hackernoon.com/raspberry-pi-headless-install-462ccabd75d0


## config

recomended

### change hostname 

via ```sudo raspi-config```

### create user

```
adduser username
usermod -aG sudo username
```

### delete pi default user

```
userdel -r pi
```

### let ansible do its magic (if configured)

```
ansible-playbook --limit ans_vanilla_pi site.yml -KbD --ask-pass
```