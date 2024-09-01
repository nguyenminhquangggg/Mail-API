# Mail-API
Install Mail API

Install Docker
```
sudo apt update -y && apt upgrade -y && sudo apt install apt-transport-https ca-certificates curl software-properties-common && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && sudo apt update && sudo apt-cache policy docker-ce && sudo apt install docker-ce -y && sudo systemctl status docker && docker info
```

```
sudo systemctl stop postfix
```

```
sudo systemctl disable postfix
```

```
git clone https://github.com/hppanpaliya/React-TrashMail.git
```

```
cd React-TrashMail
```

```
docker build -t trashmail-app .
```

```
sudo docker run -d -p 4000:4000 -p 25:25 -v ./attachments:/React-TrashMail/mailserver/attachments -e REACT_APP_API_URL= -e REACT_APP_DOMAINS='["0xf5.site", "0xf5.xyz", "0x-sync.xyz", "nodegenius.xyz"]' --name trashmail-container hppanpaliya/react-trashmail:latest
```
