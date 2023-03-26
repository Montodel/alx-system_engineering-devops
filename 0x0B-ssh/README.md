---
<h1 align="center">0x0B. SSH</h1>

---

## Description
Repository to study the following Topic: How to access a remote server with ssh using a public key

- What is a server
- Where servers usually live
- What is SSH
- How to create an SSH RSA key pair
- How to connect to a remote host using an SSH RSA key pair
- The advantage of using #!/usr/bin/env bash instead of /bin/bash

## Tasks :clipboard:

:zero: **[Use a private key](../0-use_a_private_key)**
       - Bash script that uses `ssh` to connect to the school provided server.

:one: **[Create an SSH key pair](../1-create_ssh_key_pair)**
      - Bash script that creates an RSA key pair.

:two: **[Client configuration file](../2-ssh_config)**
      - SSH configuration file configured to use the private key `~/.ssh/school and to refuse authentication using a password.

:four: **[Client configuration file](../100-puppet_ssh_config.pp)** 
       - Making changes to SSH configuration file using Puppet. The ssh_config file is configured to use private key and refuse password authentication.
