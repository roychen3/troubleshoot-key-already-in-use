# Troubleshoot: Key already in use

> [time= 2023 09 15]

1. Generating a new SSH key
```sh
$ ssh-keygen
```
set file name: `id_rsa_other_name`

<br />

2. create `~/.ssh/config`
```
Host github.other_name
    Hostname github.com
    IdentityFile=your_path/.ssh/id_rsa_other_name
```

<br />

3. Done
```sh
# clone
$ git clone git@github.other_name:your_repo.git

# or set
$ git remote set-url origin git@github.other_name:your_repo.git
```
