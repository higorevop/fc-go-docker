# Desafio Full Cycle com Go e Docker

Este repositório contém a solução para o desafio proposto, que consiste em criar uma imagem Docker que, ao ser executada, exibe a mensagem "Full Cycle Rocks!!". A imagem foi construída utilizando a linguagem de programação Go e tem menos de 2MB.

## Requisitos

- [Docker](https://www.docker.com/) instalado
- [Go](https://golang.org/) instalado (para compilar e testar localmente)

## Como usar

Para executar a imagem Docker, siga os passos abaixo:

1. Baixe a imagem do Docker Hub:
```
docker pull higorevop/fullcycle
```
2. Execute a imagem:
```
docker run higorevop/fullcycle
```

Isso deve exibir a mensagem "Full Cycle Rocks!!".

## Como compilar e testar localmente

1. Clone este repositório:
```
git https://github.com/higorevop/fc-go-docker.git
cd fullcycle-go
```

2. Compile o programa Go para um binário estático:
```
CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o fullcycle main.go
```
3. Verifique se o binário foi criado com sucesso e se tem menos de 2MB:
```
ls -lh fullcycle
```
4. Execute o binário para ver a mensagem "Full Cycle Rocks!!":
```
./fullcycle
```