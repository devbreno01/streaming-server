
## AUTH

#### Dentro desta pasta, o foco principal é realizar a autenticação do usuário ao tentar fazer login no servidor RTMP.

###### Dentro desta pasta, temos os arquivos:

```plaintext
auth/
├── node_modules/
├── .gitignore
├── Dockerfile
├── package-lock.json
├── package.json
└── server.js
```

###### O arquivo mais importante aqui é o server.js
- Nele criamos essa rota que faz a comparação com chave passada, autorizando ou não a conexão com o servidor rtmp 

```plaintext
app.post("/auth", function (req, res) {
  
  const streamkey = req.body.key;

    if (streamkey === "supersecret") {
    res.status(200).send();
    return;   
  }
  res.status(403).send();
});

```
#### Como explicitado acima, a chave para acessar a rota é 'supersecret'. Caso esteja correta, retornamos um código 200. Caso contrário, retornamos um código 403.




