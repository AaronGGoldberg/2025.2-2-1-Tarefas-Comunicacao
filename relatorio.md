# Relato da atividade de comunicação entre processos usando sockets

## Informações gerais
- **disciplina**: Sistemas operacionais
- **semestre letivo**: 2025.2
- **aluno**: Aaron Guerra Goldberg

## Parte 1 — 1 servidor e 1 cliente (bloqueante)

Executei o servidor com `python3 src/servidor.py` e ele iniciou corretamente, ficando na porta 5000 aguardando conexão.

Em seguida executei o cliente com `python3 src/cliente.py`. O cliente conectou imediatamente ao servidor.

Enviei uma mensagem ("Olá, meu amigo Servidor") e foi respondida pelo servidor no formato "Echo: <mensagem>". O servidor exibiu a mensagem recebida no terminal.

Finalizei o cliente digitando "sair", e o servidor permaneceu ativo, aguardando novas conexões. Encerramento limpo, sem erros ou exceções.

## Parte 2 — 1 servidor e 2 clientes (bloqueante)

Executei dois clientes simultaneamente conectando no mesmo servidor.

Observei que o servidor só atende um cliente por vez. Quando o cliente 1 enviou uma mensagem, o cliente 2 ficou aguardando até que a interação do cliente 1 fosse finalizada.

Não houve exceções, mas foi possível ver claramente que o processamento é serializado: as mensagens aparecem no log do servidor na ordem em que foram atendidas, nunca ao mesmo tempo.
