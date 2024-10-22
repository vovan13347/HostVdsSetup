# HostVdsSetup
____
ssh `root@XX.XX.XX.XXX`(адрес сервера) - подключение к серверу

sudo apt install wget curl -y

curl -fsSL https://code-server.dev/install.sh | sh

sudo systemctl enable --now code-server@$USER

nano ~/.config/code-server/config.yaml

sudo systemctl restart code-server@$USER

# ssh config
____
```
Host XX.XX.XX.XXX(адрес сервера)
  HostName XX.XX.XX.XXX

Host XX.XX.XX.XXX
HostName XX.XX.XX.XXX
User newuser
IdentityFile ~/.ssh/id_rsa
PreferredAuthentications publickey,password
```
# code-server config.yaml
____
```
bind-addr: 0.0.0.0:8080
auth: password
password: "пароль"
cert: false
```
