# windows_playbook_ansible

In order to setting Windows to accept connection from Ansible on Linux machine follow the istruction_below:


download ConfigureRemotingForAnsible.ps1 and run this PowerShell script without any parameters on Windows machine
https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1


On windows Machine check firewall rules in order to accept WinRM Connection on Https (port 5986)

Create on Linux Machine in your playbook directory group_vars and inside the windows.yaml

windows.yaml

---
ansible_user: Administrator
ansible_password: xxxxxxxxx
ansible_port: 5986
ansible_connection: winrm
ansible_winrm_server_cert_validation: ignore


Test windows connection from Linux to Windows Server

ansible -i hosts windows -m win_ping

Install chocolatey on windows machine to manage packages through cli and windows module

https://chocolatey.org/

Enjoy!

