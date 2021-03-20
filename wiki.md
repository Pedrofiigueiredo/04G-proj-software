# CLKP Developers

### Index

- [CLKP Developers](#clkp-developers)
    - [Index](#index)
    - [Grupo](#grupo)
    - [Descrição](#descrição)
  - [📌 Entendendo o cenário de negócio da aplicação](#-entendendo-o-cenário-de-negócio-da-aplicação)
    - [Atores](#atores)
    - [Lista de Atividades](#lista-de-atividades)
    - [Fluxo das atividades](#fluxo-das-atividades)
- [📌 Diagrama de casos de uso](#-diagrama-de-casos-de-uso)

### [Grupo](https://github.com/Pedrofiigueiredo/CLKP-developers/wiki/Grupo)

### Descrição

**Tema escolhido:** (1) Alguém compra coisas de outro alguém mediante pagamento e entrega.
 
A **CLKP** é uma loja virtual de **produtos eletrônicos**, no estilo _marketplace_, ou seja, várias lojas podem se cadastrar no site e vender seus produtos.

## 📌 Entendendo o cenário de negócio da aplicação

### Atores

Quem e o que tem interação com o negócio:

- **Clientes**: usuários do site
- **Vendedores**: lojas cadastradas na plataforma
- **Entregador**: o **serviço externo** que vai fazer o pedido chegar até o cliente (**Correios**, **FedEx**...)

### Lista de Atividades

| Atores         | Atividades                             |
|----------------|----------------------------------------|
| **Cliente**    | Procurar e comprar produtos            |
| **Vendedor**   | Adicionar produtos e atender clientes  |
| **Entregador** | Receber e entragar produto             |

### Fluxo das atividades

<img src="https://github.com/Pedrofiigueiredo/CLKP-developers/blob/main/assets/BPMN.jpeg" width="1000" />

Das várias formas possíveis de organizar o fluxo de atividades do negócio, escolhemos a **BPMN** (_Business Process Model and Notation_), para deixar bem claro qual o percurso de cada ator dentro da aplicação. Usamos o [Whimsical](https://whimsical.com/a) para construir o diagrama simultanemanete.

# 📌 Diagrama de casos de uso

![Diagrama de casos de uso](https://github.com/Pedrofiigueiredo/CLKP-developers/blob/main/assets/Casos-de-uso.png)



