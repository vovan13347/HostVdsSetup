# HostVdsSetup

ssh root@0.0.0.0 - подключение к серверу

sudo apt install wget curl -y

curl -fsSL https://code-server.dev/install.sh | sh

sudo systemctl enable --now code-server@$USER

nano ~/.config/code-server/config.yaml

sudo systemctl restart code-server@$USER

# ssh config
```
Host 31.15.17.243
  HostName 31.15.17.243

Host 31.15.17.243
HostName 31.15.17.243
User user1
IdentityFile ~/.ssh/id_rsa
PreferredAuthentications publickey,password
```
