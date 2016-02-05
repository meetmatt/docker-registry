# Private docker registry ansible playbooks

## Step 1

Prepare a remote host with publicly resolvable domain name (required to obtain Let's Encrypt SSL certs). 
Note: I haven't tested it with free domains (.tk, .gl, etc.), please report if you have.

## Step 2

Install ansible, create hosts inventory.

## Step 3 (optional)

Create remote sudo user and disable root ssh access:

```
$ ./user.yml
```

## Step 4

Install docker registry:

```
$ ./install.yml
```

## Step 5

After 3 months you will have to reissue SSL certificates manually:

```
$ ./reissue.yml
```