[![CI](https://github.com/de-it-krachten/ansible-role-brave/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-brave/actions?query=workflow%3ACI)


# ansible-role-brave

Installs Brave browser 



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- OracleLinux 9
- AlmaLinux 8
- AlmaLinux 9
- SUSE Linux Enterprise 15<sup>1</sup>
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Fedora 40
- Fedora 41

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>

</pre></code>

### defaults/family-Debian.yml
<pre><code>
brave_url: https://brave-browser-apt-release.s3.brave.com/

brave_gpg_url: https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

brave_gpg_file: /usr/share/keyrings/brave-browser-archive-keyring.gpg

brave_packages:
  - brave-browser
</pre></code>

### defaults/family-RedHat.yml
<pre><code>
brave_url: https://brave-browser-rpm-release.s3.brave.com/x86_64/

brave_gpg_url: https://brave-browser-rpm-release.s3.brave.com/brave-core.asc

brave_packages:
  - brave-browser
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'brave'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'brave'
      ansible.builtin.include_role:
        name: brave
</pre></code>
