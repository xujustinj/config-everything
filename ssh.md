# Configure SSH

## Generate a Default SSH Key

```sh
ssh-keygen
cat ~/.ssh/id_rsa.pub
```

## Copying Keys From Elsewhere

> See also: [Using Same SSH Private Key Across Multiple Machines](https://serverfault.com/a/170683)

You can copy SSH private and public keys between machines.
In order to use the keys after copying, make sure the files have the right owner and permissions:

```sh
chown ${USER}:${USER} PRIVATE_KEY PUBLIC_KEY
chmod 600 PRIVATE_KEY
chmod 644 PUBLIC_KEY
```
