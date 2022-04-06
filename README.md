
# Chat Services

Um conjunto de serviços conectados via rabbitmq para a utilização em uma aplicação de um chat ponta a ponta.

## Funcionalidades

- Envio de mensagens em tempo real sem persistência
- Chamada de Voz e vídeo (WIP)

## Apêndice

- Sender Service serve como o ponto de entrada do sistema, onde irá enviar as mensagens para a fila que o receiver service irá consumir.
- Receiver Service serve como consumidor da fila de mensagens e encarregado de enviar essa mensagem para o front-end via websocket.

## Documentação da API (SenderService)

### Retorna todos os itens

```http
  POST /message/send
```

| Body   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `content` | `string` | **Obrigatório**. Mensagem enviada |
| `sender` | `string` | **Obrigatório**. uuid do usuário que enviou a mensagem |
| `receiver` | `string` | **Obrigatório**. uuid do usuário receptor da mensagem |

## Links

- [Sender Service](https://github.com/RodolfoBonis/chat_send_service)
- [Receiver Service](https://github.com/RodolfoBonis/chat_receive_service)

## Stack utilizada

**Front-end:** Flutter

**Back-end:** Golang, Gin-gonic, rabbitmq, websocket

## Autores

- [@RodolfoBonis](https://github.com/RodolfoBonis)
