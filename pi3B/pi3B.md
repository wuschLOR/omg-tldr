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

1. select ```2 Network Options      Configure network settings```
2. select ```N1 Hostname                Set the visible name for this Pi on a network```
3. OK
4. enter hostname that is unique and can be rememberd

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
ansible-playbook --limit ans_vanilla_pi_user site.yml -KbD --ask-pass
```