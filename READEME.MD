
## RODANDO O SERVIDOR LIVESTREAM 

### PRÉ REQUISITOS
```http
    OBS STUDIO 
    VLC media player
    Node e npm 
    Nginx 
    Docker
```


#### Após clonar o projeto, esse é o passo a passo:

##### Rode na pasta auth

```http
 npm install
```

##### Depois rode os comandos docker na root

```http
 docker-compose build
```

```http
 docker-compose up
```
##### URL para acessar a live stream OBS é 
```http
  rtmp://localhost:1935/live
```

##### key para acessar a live stream OBS é 
```http
  abdi?key=supersecret
```

##### Acessar a live no VLC, chama-se pela url:
```http
  rtmp://localhost:1935/live/abdi
```

### Pespectivas de melhoria 
 - Entender protocolo HLS para conversão no nginx 
 