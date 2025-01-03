#mongoengine教學
##使用Debian GNU/Linux

這次要來讓大家可以讓網頁資料持久化的模組mongoengin，首先先安裝:

```

for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done

sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y

sudo apt-get update
sudo apt-get install make -y

```


接下來創一個檔案，檔名是docker-compose.yaml，然後放入:

```
services:
  mongodb:
    image: "mongo:latest"
    container_name: mongodb
    environment:
      MONGO_INITDB_ROOT_USERNAME: root
      MONGO_INITDB_ROOT_PASSWORD: abc123
    ports:
      - "127.0.0.1:27017:27017"
    volumes:
      - ./data:/data/db
```
接下來存檔退出，接著輸入打開，還有裝模組:
```
python3 -m pip install mongoengine==0.29.1
sudo docker compose up -d
```
接下來創一個檔名為user_odm.py的檔案，放入:
```
import mongoengine as me
from mongoengine.queryset.manager import QuerySetManager
class User(me.Document):
    objects: QuerySetManager

    id = me.SequenceField(primary_key=True)
    name = me.StringField(max_length=255, required=True)

```
大家可以自行修改，接下來輪到我們app.py了，如果要放入東西的話:
```
user = User(name=id)
user.save()
```
那如果要讀取:
```
User.objects(name=id).first()
```
基本上就是這樣子就可以解決囉

![](https://i.imgur.com/RCdfwVa.png)

