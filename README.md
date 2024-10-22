# HostVdsSetup
____
ssh root@0.0.0.0(адрес сервера) - подключение к серверу

sudo apt install wget curl -y

curl -fsSL https://code-server.dev/install.sh | sh

sudo systemctl enable --now code-server@$USER

nano ~/.config/code-server/config.yaml

sudo systemctl restart code-server@$USER

# ssh config
____
```
Host 0.0.0.0(адрес сервера)
  HostName 0.0.0.0

Host 0.0.0.0
HostName 0.0.0.0
User user1
IdentityFile ~/.ssh/id_rsa
PreferredAuthentications publickey,password
```
