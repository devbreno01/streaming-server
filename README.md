## Servidor Livestream

### Pré-requisitos

```http
OBS Studio
Node.js e npm
Nginx
Docker
```

### Passo a passo após clonar o projeto

#### 1. Acesse a pasta `auth`
```bash
cd auth
```

#### 2. Instale as dependências
```bash
npm install
```

#### 3. Rode os comandos Docker na pasta raiz do projeto

Construa os containers:
```bash
docker-compose build
```

Inicie os containers:
```bash
docker-compose up
```

#### 4. URL para acessar a live stream no OBS
```http
rtmp://localhost:1935/live
```

#### 5. Chave de transmissão (KEY) para o OBS

Para conectar à rede via OBS, é necessário inserir uma chave de transmissão, que funciona como uma medida de segurança. No OBS, insira a chave no campo "Chave de transmissão".

```http
Chave:
abdi?key=supersecret
```

#### 6. Acesse a live no navegador pela URL
```http
GET
http://localhost:8080/
```


