# controle-sala-py

Sistema de controle concorrente de acesso a uma sala de reuniões com capacidade limitada, utilizando Python, Sockets, Threads e Semáforos.

---

## Participantes

- Gustavo Souto Pereira  
- Ian Felipe Souza Alves  
- Ithallo Leandro Rodrigues Barbosa  
- João Victor Campos Costa  
- Lucas Homero Vieira dos Santos  

---

## Projeto Acadêmico

Desenvolvido para a disciplina de Programação Concorrente e Distribuída, 5º semestre de Ciência da Computação, Universidade Católica de Brasília (UCB/DF).

---

## Objetivo

Simular um sistema de controle de acesso a uma sala com capacidade máxima de 5 pessoas, garantindo que:
- Não ocorra superlotação.
- A entrada e saída sejam tratadas de forma concorrente e segura.
- Múltiplos clientes possam interagir com o servidor ao mesmo tempo.

---

## Tecnologias e Conceitos Utilizados

- Python 3
- socket (comunicação TCP)
- threading (concorrência com múltiplos clientes)
- Semaphore (controle de acesso simultâneo)
- Terminal como interface interativa

---

## Estrutura do Projeto

```
controle-sala-py/
├── cliente.py       # Cliente que tenta entrar ou sair da sala
├── servidor.py      # Servidor que controla o acesso à sala
└── README.md        # Documentação do projeto
```

---

## Como Executar

1. Clone o Repositório
```bash
git clone https://github.com/seu-usuario/controle-sala-py.git
cd controle-sala-py
```

2. Inicie o servidor
```bash
python servidor.py
```

3. Inicie o(s) cliente(s) em outro(s) terminal(is)
```bash
python cliente.py
```

Você pode abrir várias instâncias de clientes para simular acesso simultâneo à sala.

---

## Funcionamento

- A sala tem capacidade máxima de 5 pessoas.
- Se um cliente tentar entrar e houver vaga, o acesso é permitido.
- Se a sala estiver cheia, o cliente será informado.
- Ao sair, o cliente libera vaga para outros entrarem.
- O sistema exibe em tempo real a quantidade de ocupantes.

---

## Exemplo de Execução

```
[ENTROU] ('127.0.0.1', 52144) | Total na sala: 3/5
[BLOQUEADO] ('127.0.0.1', 52145) tentou entrar | Sala cheia (5/5)
[SAIU] ('127.0.0.1', 52142) | Total na sala: 4/5
```


