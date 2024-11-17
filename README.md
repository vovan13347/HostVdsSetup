# HostVdsSetup
____
`ssh root@XX.XX.XX.XXX`(адрес сервера) - подключение к серверу

sudo apt install wget curl -y

curl -fsSL https://code-server.dev/install.sh | sh

sudo systemctl enable --now code-server@$USER

nano ~/.config/code-server/config.yaml

sudo systemctl restart code-server@$USER

adduser username - добавление пользователя

sudo iptables -A INPUT -p tcp --dport 5000 -j ACCEPT
sudo sh -c "iptables-save > /etc/iptables/rules.v4"

curl localhost:5000

sudo iptables -I INPUT -p tcp --dport 5000 -j ACCEPT

sudo iptables -I INPUT -p udp --dport 5000 -j ACCEPT


sudo ufw status
sudo iptables -L
sudo systemctl status firewalld



sudo netstat -tuln
flask run --host=0.0.0.0 --port=5000

export FLASK_RUN_HOST=0.0.0.0

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
