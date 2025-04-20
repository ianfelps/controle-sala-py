# controle-sala-py
Sistema de controle concorrente de acesso a uma sala de reuniões com capacidade limitada, utilizando Python, Sockets, Threads e Semáforos.

---

## Projeto Acadêmico

Desenvolvido para a disciplina de Programação Concorrente e Distribuída, 5º semestre de Ciência da Computação, Universidade Católica de Brasília (UCB/DF).

---

## Participantes

- Gustavo Souto Pereira  
- Ian Felipe Souza Alves  
- Ithallo Leandro Rodrigues Barbosa  
- João Victor Campos Costa  
- Lucas Homero Vieira dos Santos  

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

## Objetivo

Simular um sistema de controle de acesso a uma sala com capacidade máxima de 5 pessoas, garantindo que:
- Não ocorra superlotação.
- A entrada e saída sejam tratadas de forma concorrente e segura.
- Múltiplos clientes possam interagir com o servidor ao mesmo tempo.

---

###  Instruções de Execução

#### **Pré-requisitos**
- Python 3.x instalado no sistema
- Terminais separados para servidor e clientes

---

#### **1. Iniciar o Servidor**
Abra um terminal e execute:

```bash
python servidor.py
```

O servidor escutará na porta `12345` e exibirá todas as operações realizadas (entradas, saídas, tentativas de acesso etc.).

---

#### **2. Iniciar um Cliente**
Em outro terminal (ou vários, se desejar simular múltiplos usuários), execute:

```bash
python cliente.py
```

Você verá um menu com as opções:

```
--- MENU ---
1. Entrar na sala
2. Sair da sala
3. Sair do programa
```

Digite o número da opção desejada e pressione Enter.

---

#### **3. Funcionamento**
- A sala comporta **até 5 pessoas** simultaneamente.
- Se a sala estiver cheia, a entrada será bloqueada.
- Ao sair, o sistema libera espaço para outro cliente.

---

#### **4. Encerrando o sistema**
- Clientes devem escolher a opção `3` para encerrar sua sessão.

---

## Exemplo de Execução

```
[ENTROU] ('127.0.0.1', 52144) | Total na sala: 3/5
[BLOQUEADO] ('127.0.0.1', 52145) tentou entrar | Sala cheia (5/5)
[SAIU] ('127.0.0.1', 52142) | Total na sala: 4/5
```
