## 一、docker code

### 1.mc

```shell
docker run -idt \
    -v /home/minecraft/data/CreateAstral:/data \
    -e TYPE=CURSEFORGE \
    -e ANNOUNCE_PLAYER_ACHIEVEMENTS=TRUE \
    -e VERSION=1.18.2 \
    -e MEMORY=4g \
    -e CF_SERVER_MOD=CreateAstral.zip \
    -e EULA=TRUE \
    -e CF_BASE_DIR=/data \
    -p 25565:25565 \
    --name createAstral itzg/minecraft-server:java17
    
    
docker exec mc mc-send-to-console op player
```

```shell
docker run -d \
	-v /home/minecraft/data/WightCraft:/data \
    -e TYPE=FABRIC \
    -p 25565:25565 \
    -e EULA=TRUE \
    -e VERSION=1.19 \
    -e MEMORY=4g \
    -e FABRIC_LAUNCHER='Wightcraft v0.98.4.jar' \
    --name wightcraft itzg/minecraft-server:java8-openj9
	
```

