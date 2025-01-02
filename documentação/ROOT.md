# ROOT

## docker-compose.yml

O arquivo `docker-compose.yml` que orquestra dois serviços Docker: um servidor RTMP e um servidor de autenticação. O objetivo desse `docker-compose` é fornecer uma configuração simples para rodar ambos os serviços, que podem ser usados para streaming de vídeo e controle de autenticação.

## Estrutura do Arquivo `docker-compose.yml`

O arquivo `docker-compose.yml` contém a seguinte configuração:

### 1. Serviço `rtmp`

O serviço `rtmp` configura um servidor de transmissão em tempo real (RTMP), que pode ser usado para enviar fluxos de vídeo para a web.

- **Diretório de build**: `./rtmp`  
  O diretório `./rtmp` contém o código necessário para construir a imagem Docker do servidor RTMP. Certifique-se de ter os arquivos de configuração adequados nesse diretório.
  
- **Portas**:
  - `1935:1935`: A porta padrão RTMP para streaming de vídeo.
  - `8080:8080`: Porta para acesso a uma interface web, caso configurada.
  
- **Nome do Container**: `rtmp_server`  
  O nome do container gerado será `rtmp_server`.

- **Volumes**: 
  - `./data:/tmp/hls`: O volume mapeia o diretório `./data` para o diretório `/tmp/hls` no container. Isso é útil para armazenar e acessar os vídeos transmitidos.

### 2. Serviço `auth`

O serviço `auth` é responsável pela autenticação dos usuários que interagem com o servidor RTMP.

- **Diretório de build**: `./auth`  
  O diretório `./auth` contém o código para o servidor de autenticação.

- **Nome do Container**: `auth_server`  
  O nome do container gerado será `auth_server`.

