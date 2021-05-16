# Cliente

# CDU01 - Acessar catálogo de produtos

#### Aluno: Pedro Figueiredo Dias
#### TIA: 41990455

<br>

## Protótipo de tela
![Tela de catálogo de produtos parte 1](../assets/telas/CDU01%20-%20Acessar%20catálogo%20de%20produtos.png)
![Tela de catálogo de produtos parte 2 - menu](../assets/telas/CDU01%20-%20Menu.png)
![Tela de catálogo de produtos parte 3 - produto específico](../assets/telas/CDU01%20-%20Olhar%20produto%20específico.png)

<br>

## Fluxograma de negócio
![Fluxo acessar catalogo de produtos](../assets/casos/1-acessar-catalogo-produtos.jpeg)

---
<br>

## Especificação do caso de uso

## Especificação do caso de uso
<br> | CDU01 - Acessar catálogo de produtos
---|---
**Descrição** | O cliente entra na página principal do sistema para olhar produtos, pesquisar <br>por itens específicos e adicionar ao carrinho. Qualquer cliente pode acessar o catálogo, <br>mas somente clientes logados podem efetuar compras.
**Nível** | Objetivo do cliente
**Ator principal** | Cliente
**Pré-condições** | -
**Pós-condições** | Cliente pode adicionar produtos ao carrinho

<br>

#### Fluxo principal

Ações do **cliente** | Ações do **sistema**
--|--
(1) Acessa o site do catálogo de produtos | (2) Apresenta para o cliente os produtos disponíveis do catálogo | 
(3) Adiciona produtos ao carrinho | (4) Redireciona cliente para a página de login
(4) Efetua login | (5) Adiciona produto escolhido ao carrinho do cliente

<br>

#### Fluxos alternativos

- Cliente pode adicionar pedido ao carrinho
  - Cliente cria conta ou faz login
- Cliente pode acessar página de “Meus Pedidos” para ver todos os pedidos feitos

<br>

[próximo](#cdu02---criar-conta-cliente)

<br><br>

# CDU02 - Criar conta cliente

#### Aluno: Pedro Figueiredo Dias
#### TIA: 41990455

<br>

## Protótipo de tela
![Tela de criar conta cliente parte 1](../assets/telas/CDU02%20-%20p1%20Cadastrar%20conta%20cliente.png)
![Tela de criar conta cliente parte 2](../assets/telas/CDU02%20-%20p2%20Cadastrar%20conta%20cliente.png)

<br>

## Fluxograma de negócio
![Fluxo criar conta cliente](../assets/casos/2-criar-conta-cliente.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU02 - Acessar catálogo de produtos
---|---
**Descrição** | O cliente precisa se cadastrar para poder fazer compras na CLKP
**Nível** | Objetivo do cliente
**Ator principal** | Cliente
**Pré-condições** | Cliente precisa ter endereço de email e CPF
**Pós-condições** | Conta foi criada. O cliente tem acesso ao catálogo de produtos e pode fazer compras.

<br>

### Fluxo principal

Ações do **cliente** | Ações do **sistema**
--|--
(1) O cliente acessa o site do sistema na página de criação de conta; | <br>
(2) O cliente insere o nome completo, um email e uma senha; | (3) O sistema verifica se o email é válido e a senha é forte o suficiente ;
<br> | (4) Sistema apresenta tela com mais informações cadastrais;
(5) Cliente insere CPF e informações de endereço; | <br>
(6) Cliente aceitar termos e política do sistema; | <br>
(7) Cliente finaliza criação de conta;  <br> | (8) Sistema verifica se o CPF é válido; <br> 
<br> | (9) Sistema efetua criação de conta do cliente e manda um email de notificação;
<br> | (10) Sistema redireciona cliente para a página de catálogo de produtos.

<br>

### Fluxos alternativos
#### 3a. Cliente insere email inválido: <br>
Ações do cliente | Ações do sistema
--|--
<br> | (1) Sistema exibe mensagem de “email inválido” para cliente e<br> pede que insira um email válido;
(2) Cliente corrige o email. | <br>

<br>

#### 3b. Cliente insere senha fraca (com menos de 8 caracteres e sem letra maiúscula):
Ações do cliente | Ações do sistema
--|--
<br> | (1) Site do sistema exibe mensagem “senha inválida” para cliente<br> e pede ao cliente inserir uma senha mais forte;
(2) Cliente corrige a senha. | <br>

<br>

#### 6a. Cliente não aceitou termos e política do sistema
Ações do cliente | Ações do sistema
--|--
<br> | (1) Sistema exibe mensagem “Para se registrar, você precisa<br> aceitar termos e políticas do sistema”
(2) Cliente aceita termos e política de uso |

<br>

#### 8a. Cliente insere CPF inválido
Ações do cliente | Ações do sistema
--|--
<br> | (1) Sistema exibe mensagem “insira um CPF válido”
(2) Cliente corrige o CPF | 

<br>

[< anterior]() | [próximo >]()

<br><br>

# CDU03 - Efetuar compra

#### Aluno: Pedro Figueiredo Dias
#### TIA: 41990455

<br>

## Protótipo de tela
![Tela de efetuar compra]()

<br>

## Fluxograma de negócio
![Fluxo efetuar compra](../assets/casos/3-efetuar-compra.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU03 - Efetuar compra
---|---
**Descrição** | Situação em que o cliente já escolheu os produtos que deseja, já os adicionou <br>ao carrinho e está pronto para informar os dados de pagamento e efetivar a compra.
**Nível** | Objetivo do cliente
**Ator principal** | Cliente
**Pré-condições** | Cliente deve ter adicionado um ou mais produtos ao carrinho. <br>Cliente deve ter conta na plataforma e estar logado.
**Pós-condições** | O sistema processa o pedido e envia para o sistema externo de pagamento.

<br>

### Fluxo principal
Ações do **cliente** | Ações do **sistema** | Ações da loja
--|--|--
(1) O cliente adiciona a quantidade de produtos que deseja ao carrinho | <br> | 
(2) O cliente seleciona as opções exigidas para cada produto no carrinho (cor, quantidade) | <br> |
(3) Cliente acessa a página de carrinho que mostra os produtos adicionados | (4) Sistema preenche endereço de entrega com os dados da conta do cliente |
(5) Cliente seleciona forma de pagamento e fornece os dados necessários | <br> |
(6) Cliente efetua compra | (7) Sistema envia dados de pagamento para serviço de pagamento |
<br> | (8) Sistema atualiza o status do pedido para “Pagamento efetuado” | <br>
<br> | (9) Sistema notifica o cliente por email sobre a atualização no status. | <br>
<br> | <br> | (10) A loja recebe o pedido.

<br>

### Fluxos alternativos

#### 4a. Cliente deseja trocar o endereço
Ações do **cliente** | Ações do **sistema**
--|--
<br> | (1) Sistema apresenta campos para inserir logradouro, número, <br>bairro, cidade, complemento e ponto de referência
(2) Cliente preenche os dados e confirma a alteração de endereço | 
 
#### 5a. Pagamento em boleto
Ações do **cliente** | Ações do **sistema** | Ações do sistema de pagamento
--|--|--
<br> | (1) O sistema solicita o boleto ao serviço de pagamento <br>e disponibiliza para o cliente; |
(2) Cliente efetuar o pagamento; | <br> | (3) Sistema de pagamento aguarda o pagamento ser <br>efetuado (em média 3 dias para o boleto ser debitado);
#br> | (4) Volta para o passo 8 do fluxo principal. |

#### 5b. Pagamento em cartão de crédito
Ações do **cliente** | Ações do **sistema** | Ações do sistema de pagamento
--|--|--
<br> | (1) Sistema pede as informações do cartão (número do cartão, nome do titular,<br>código de segurança e data de validade); |
(2) Cliente seleciona o número de parcelas para o pagamento; | <br> | (3) Sistema de pagamento aguarda o pagamento<br> ser efetuado;
#br> | (4) Volta para o passo 8 do fluxo principal. |

#### 5c. Pagamento em cartão de débito
Ações do **cliente** | Ações do **sistema** | Ações do sistema de pagamento
--|--|--
<br> | (1) Sistema pede as informações do cartão (número do cartão, nome do titular, <br>código de segurança e data de validade); |
(2) Cliente seleciona o número de parcelas para o pagamento; | <br> | (3) Sistema de pagamento aguarda o pagamento<br> ser efetuado;
#br> | (4) Volta para o passo 8 do fluxo principal. |

#### 5d. Cliente insere dados de pagamento inválidos
Ações do **cliente** | Ações do **sistema**
--|--
<br> | (1) Sistema exibe mensagem “dados inválidos” ao cliente e pede ao cliente inserir os dados válidos;
#2) Cliente corrige as informações; | (3) Volta para o passo 6 do fluxo principal.

#### 8a. Pagamento reprovado
Ações do **cliente** | Ações do **sistema**
--|--
<br> | (1) Sistema envia email para o cliente informando que o pagamento não foi aprovado
#2) Cliente acessa o link do email; | (3) Volta para o passo 4 do fluxo principal.

[< anterior]() | [próximo >]()

<br><br>

# CDU04 - Acompanhar pedido

#### Aluno: Pedro Figueiredo Dias
#### TIA: 41990455

<br>

## Protótipo de tela

![Tela com menu](../assets/telas/CDU01%20-%20Menu.png)
![Tela de acompanhar pedido parte 1](../assets/telas/CDU04%20-%20p1%20Acompanhar%20pedido.png)
![Tela de acompanhar pedido parte 2](../assets/telas/CDU04%20-%20p2%20Acompanhar%20pedido.png)

<br>

## Fluxograma de negócio
![Fluxo acompanhar pedido](../assets/casos/4-acompanhar-pedido.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU04 - Acompanhar pedido
---|---
**Descrição** | Depois de ter feito um pedido, o cliente pode acompanhar o status do envio, <br>para ter uma estimativa da data de entrega e a localização do pedido, assim como ter <br>acesso a eventuais atrasos. Os possíveis status do pedido são: Pagamento efetuado, <br>Pedido recebido, Enviado a transportadora, Entregue, Cancelado
**Nível** | Objetivo do cliente
**Ator principal** | Cliente
**Pré-condições** | O cliente deve ter, no mínimo, uma compra efetuada.
**Pós-condições** | O sistema apresenta ao cliente o status do pedido.

<br>

### Fluxo principal
Ações do **cliente** | Ações do **sistema**
--|--
(1) Cliente acessa página acompanhar pedido; | (2) Sistema apresenta lista de pedidos do cliente;
(3) Cliente seleciona o pedido que deseja acompanhar; | (4) Sistema apresenta status do pedido.

<br>

### Fluxos alternativos
- 

[< anterior]() | [próximo >]()

<br><br>


# CDU05 - Cancelar pedido

#### Aluno: Pedro Figueiredo Dias
#### TIA: 41990455

<br>

## Protótipo de tela

Cancelar pedido é uma opção que aparece na tela de "Acompanhar pedido" **somente quando o status é inferior à "Pedido recebido"**, porque depois que a loja envia à transportadora não é mais possível cancelar.

![Tela de cancelar pedido](../assets/telas/CDU05%20-%20Cancelar%20pedido.png)

<br>

## Fluxograma de negócio
![Fluxo cancelar pedido](../assets/casos/5-cancelar-pedido.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU05 - Cancelar pedido
---|---
**Descrição** | Por qualquer motivo o cliente decide cancelar a entrega do pedido
**Nível** | Objetivo do cliente
**Ator principal** | Cliente
**Pré-condições** | O status do pedido deve estar, no máximo, no estágio “Pedido recebido”.
**Pós-condições** | O pedido é cancelado.

<br>

### Fluxo principal
Ações do **cliente** | Ações do **sistema** | Ações da loja
--|--|--
(1) Cliente acessa a página de acompanhar pedido; <br> (2) Cliente cancela o pedido; | (3) Sistema duda status do pedido para cancelado; <br> (4) Sistema notifica a loja de que o pedido foi cancelado; | (5) Loja para de preparar o produto;
<br> | (6) Sistema aciona o sistema de pagamento para que efetue o estorno para o cliente; <br> (7) Sistema de pagamento envia o estorno para o cliente; <br> (8) Sistema notifica o cliente por email de que o estorno foi realizado.


<br>

### Fluxos alternativos
-

[< anterior]() | [próximo >]()

<br><br>


# CDU06 - Devolver produto

#### Aluno: Pedro Figueiredo Dias
#### TIA: 41990455

<br>

## Protótipo de tela

"Solicitar devolução" é uma opção que aparece na tela de "Acompanhar pedido" **somente depois que o status do pedido é "Entregue"**, pois não é possível que o cliente devolva algo que ele ainda não recebeu.

![Tela de devolver pedido](../assets/telas/CDU06%20-%20Devolver%20produto.png)

<br>

## Fluxograma de negócio
![Fluxo devolver produto]()

---
<br>

## Especificação do caso de uso

<br> | CDU06 - Devolver produto
---|---
**Descrição** | Caso o produto venha com defeito ou qualquer outra situação que se encaixa<br> na política de devolução, o cliente pode solicitar a devolução e receber seu dinheiro de volta.
**Nível** | Objetivo do cliente
**Ator principal** | Cliente
**Pré-condições** | O cliente deve ter recebido ao menos um produto. <br>O prazo para devolver um produto deve estar de acordo com o especificado pela<br> loja na descrição do produto e seguir as políticas de devolução da loja.
**Pós-condições** | O cliente envia de volta para a loja o produto e recebe seu dinheiro de volta.

<br>

### Fluxo principal
Ações do **cliente** | Ações do sistma | Ações do **administrador do sistema** | Ações da loja
--|--|--|--
(1) Cliente acessa página de devolver produto; <br> (2) Cliente seleciona o produto que deseja devolver; <br> (3) Cliente informa o motivo da devolução; <br> (4) Cliente solicita devolução | <br> | (5) Administrador do sistema avalia a solicitação do cliente; | <br>
<br> | (6) Sistema notifica a loja de que o pedido que será devolvido; | <br> | (7) Loja aceita a devolução;
(8) Cliente envia pedido de volta para a loja; | (9) Sistema aciona o sistema de pagamento para que devolva dinheiro ao cliente; <br> (10) Sistema de pagamento efetua o estorno para o cliente; <br> (11) Sistema notifica o cliente por email de que o estorno foi realizado. | <br> | 

<br>

### Fluxos alternativos
-

[< anterior]() | [próximo >]()

<br><br>


# CDU07 - Avaliar experiência (NPS)

#### Aluno: Pedro Figueiredo Dias
#### TIA: 41990455

<br>

## Protótipo de tela

![Tela de avaliar experiência NPS](../assets/telas/CDU07%20-%20Avaliar%20experiência.png)

<br>

## Fluxograma de negócio
![Fluxo avaliar experiencia](../assets/casos/7-avaliar-experiencia-nps.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU07 - Avaliar experiência (NPS)
---|---
**Descrição** | Essa é uma medida para avaliar a satisfação dos clientes no uso do sistema.<br> O cliente dá uma nota de 1 a 10 para sua experiência na plataforma.
**Nível** | Objetivo do cliente
**Ator principal** | Cliente
**Pré-condições** | Cliente ter efetuado uma compra
**Pós-condições** | O sistema recebe a opinião do cliente e armazena esse dado relacionado à loja responsável.<br> A loja tem acesso a resposta do cliente.

<br>

### Fluxo principal
Ações do **cliente** | Ações do sistma
--|--
<br> | (1) Sistema envia ao cliente email com um link para responder a pesquisa de avaliação;
(2) Cliente acessa o link; <br> (3) Cliente responde à pesquisa com uma nota de 1 a 10; <br> (4) Cliente opta ou não por escrever um comentário; <br> (5) Cliente responde a pesquisa; | (6) Sistema apresenta uma mensagem de agradecimento ao cliente; <br> (7) Sistema armazena esse dado.


<br>

### Fluxos alternativos
#### 2a. Cliente não abre o email:
Ações do **cliente** | Ações do sistma
--|--
<br> | (1) Sistema aguarda duas semanas e envia um novo email na tentativa de obter a resposta do cliente.


[< anterior]() | [próximo >]()

<br><br>


# CDU08 - Denunciar loja

#### Aluno: Pedro Figueiredo Dias
#### TIA: 41990455

<br>

## Protótipo de tela

![Tela de denunciar loja](../assets/telas/CDU08%20-%20Denunciar%20loja.png)

<br>

## Fluxograma de negócio
![Fluxo denunciar loja]()

---
<br>

## Especificação do caso de uso

<br> | CDU08 - Denunciar loja
---|---
**Descrição** | Essa é uma medida para avaliar a satisfação dos clientes no uso do sistema.<br> O cliente dá uma nota de 1 a 10 para sua experiência na plataforma.
**Nível** | Objetivo do cliente
**Ator principal** | Cliente
**Pré-condições** | Cliente ter efetuado uma compra
**Pós-condições** | O sistema recebe a opinião do cliente e armazena esse dado relacionado à loja responsável.<br> A loja tem acesso a resposta do cliente.

<br>

---

### Fluxo principal
Ações do **cliente** | Ações do administrador do sistema
--|--
(1) Cliente acessa a página da loja; <br> (2) Cliente informa o motivo e denuncia a loja; | (3) Administrador do sistema analisa a denúncia; <br> (4) Administrador do sistema exclui a loja da plataforma e a aciona as organizações responsáveis.



<br>

### Fluxos alternativos
#### 3a. Não há irregularidades na loja
Ações do **cliente** | Ações do administrador do sistema
--|--
<br> | (1) Desconsidera denúncia.


[< anterior]() | [próximo >]()

<br><br>

---

## Loja

# CDU9 - Criar conta loja

#### Aluno: Pedro Figueiredo Dias
#### TIA: 41990455

<br>

## Protótipo de tela

![Tela de criar conta loja parte 1](../assets/telas/CDU09%20-%20p1%20Criar%20conta%20loja.png)
![Tela de criar conta loja parte 2](../assets/telas/CDU09%20-%20p2%20Criar%20conta%20loja.png)

<br>

## Fluxograma de negócio
![Fluxo criar conta loja](../assets/casos/9-criar-conta-loja.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU9 - Criar conta loja
---|---
**Descrição** | Para uma loja poder cadastrar seus produtos e vender na CLKP ela deve ter um cadastro aprovado.<br> Nessa etapa, também, a loja escolhe o plano de pagamento para o uso da plataforma.
**Nível** | Objetivo loja
**Ator principal** | Loja
**Pré-condições** | Loja deve possuir CNPJ/MEI e endereço de email.
**Pós-condições** | Conta loja criada. A Loja poderá adicionar produtos no catálogo.

<br>

---

### Fluxo principal
Ações da loja | Ações do sistema | Ações do administrador do sistema
--|--|--
(1) Loja acessa a página de criar conta lojista; <br> (2) Loja preenche formulário com informações cadastrais; <br> (4) Loja seleciona plano de cobrança; <br> (5) Loja aceita termos e política de uso do sistema; <br> (6) Loja finaliza cadastro e solicita ser aceita no sistema; <br> | (7) Administrador do sistema analisa solicitação da loja; | (3) Sistema apresenta planos disponíveis de associação; <br> (8) Sistema envia email para a loja informando que sua solicitação foi aprovada.

<br>

### Fluxos alternativos
#### 2a. Email inválido


#### 2b. CNPJ inválido


#### 7. Administrador do sistema não aprova solicitação da loja


[< anterior]() | [próximo >]()

<br><br>

# CDU10 - Cadastrar produto

#### Aluno: Ye Wei Jiang
#### TIA: 41926293

<br>

## Protótipo de tela

![Tela de cadastrar produto](../assets/telas/CDU10%20-%20Cadastrar%20produto.png)

<br>

## Fluxograma de negócio
![Fluxo cadastrar produto](../assets/casos/10-cadastrar-produto.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU10 - Cadastrar produto
---|---
**Descrição** | A loja adicionar um produto para ser exibido e comercializado na CLKP.
**Nível** | Objetivo loja
**Ator principal** | Loja
**Pré-condições** | A loja precisa ter cadastro.<br>Loja precisa ter sido aprovada para vender produtos na plataforma. <br>A loja precisa estar logada.
**Pós-condições** | O produto é adicionado ao catálogo da loja.

<br>

---

### Fluxo principal
Ações da loja | Ações do sistema
--|--
(1) Loja acessa a página de cadastro de produtos; <br> (2) Loja adiciona informações sobre o produto (nome, preço...); <br> (3) Loja confirma adição do produto; <br> | (4) Sistema adiciona produto ao catálogo da loja.

<br>

### Fluxos alternativos
#### 2a. Informações sobre o produto inválidas


[< anterior]() | [próximo >]()

<br><br>

# CDU11 - Remover ou bloquear produto

#### Aluno: Ye Wei Jiang
#### TIA: 41926293

<br>

## Protótipo de tela

![Tela de remover ou bloquear produto](../assets/telas/CDU11%20-%20Remover%20ou%20Bloquear%20produto.png)

<br>

## Fluxograma de negócio
![Fluxo remover ou bloquear produto](../assets/casos/11-remover-ou-bloquear-produto.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU11 - Remover ou bloquear produto
---|---
**Descrição** | A loja deseja remover ou bloquear um produto para ser exibido e comercializado na CLKP.
**Nível** | Objetivo loja
**Ator principal** | Loja
**Pré-condições** | A loja precisa estar logada.
**Pós-condições** | O produto é retirado do catálogo do catálogo da loja. <br>Caso haja pedidos em andamento, eles precisam ser entregues.

<br>

---

### Fluxo principal
Ações da loja | Ações do sistema
--|--
(1) Loja acessa página com lista de produtos cadastrados; <br> (3) Loja exclui ou bloqueia temporariamente um produto; <br> (5) Loja confirma remover ou bloquear produto; | (2) Sistema exibe produtos cadastrados pela loja; <br> (4) Sistema exibe mensagem de confirmação da decisão; <br> (6) Sistema retira produto do catálogo.

<br>

### Fluxos alternativos


[< anterior]() | [próximo >]()

<br><br>


# CDU12 - Aprovar pedido

#### Aluno: Ye Wei Jiang
#### TIA: 41926293

<br>

## Protótipo de tela

![Tela de aprovar pedidos](../assets/telas/CDU12%20-%20Aprovar%20pedido%20e%20CDU13%20-%20Enviar%20pedido%20a%20transportadora.png)

<br>

## Fluxograma de negócio
![Fluxo aprovar pedido](../assets/casos/12-aprovar-pedido.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU12 - Aprovar pedido
---|---
**Descrição** | A loja confirma que o pedido foi recebido e que estará <br>preparando e logo enviará para a transportadora.
**Nível** | Objetivo loja
**Ator principal** | Loja
**Pré-condições** | Cliente precisa ter efetuado compra e o pagamento precisa ser efetivado. <br>Loja precisa estar logada no sistema.
**Pós-condições** | Loja confirma que recebeu o pedido e enviará a transportadora. <br>Sistema altera o status do pedido e notifica o cliente dessa alteração.

<br>

---

### Fluxo principal
Ações da loja | Ações do sistema
--|--
(2) Loja confirma que o produto será enviado; | (1) Sistema notifica a loja de que um cliente fez um pedido; <br> (3) Sistema atualiza status do pedido para “Pedido recebido”; <br> (4) Sistema notifica o cliente por email da alteração do status.


<br>

### Fluxos alternativos
#### 2a. Loja não aprova o pedido


[< anterior]() | [próximo >]()

<br><br>


# CDU13 - Enviar pedido a transportadora

#### Aluno: Ye Wei Jiang
#### TIA: 41926293

<br>

## Protótipo de tela

A loja pode confirmar essa opção tanto na página "Suas vendas" quanto na página da venda específica de um produto.

![Tela de enviar pedido à transportadora opção 1](../assets/telas/CDU12%20-%20Aprovar%20pedido%20e%20CDU13%20-%20Enviar%20pedido%20a%20transportadora.png)
![Tela de enviar pedido à transportadora opção 2](../assets/telas/CDU14%20-%20Suporte.png)

<br>

## Fluxograma de negócio
![Fluxo enviar pedido a transportadora](../assets/casos/13-enviar-pedido-a-transportadora.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU13 - Enviar pedido a transportadora
---|---
**Descrição** | A loja prepara o pedido do cliente (embala etc) e envia para a transportadora.
**Nível** | Objetivo loja
**Ator principal** | Loja
**Pré-condições** | Loja deve ter aprovado pedido do cliente.
**Pós-condições** | O pedido é encaminhado à transportadora. <br>O sistema altera o status do pedido e notifica o cliente dessa alteração. <br>A transportadora faz o pedido chegar ao cliente. <br>A loja recebe o pagamento pelo pedido.

<br>

---

### Fluxo principal
Ações da loja | Ações do sistema
--|--
(1) Loja separa e embala o produto do cliente; <br> (2) Loja envia o produto para a transportadora; <br> (3) Loja acessa o sistema e sinaliza que fez o envio; | (4) Sistema altera o status do pedido para “Entregue a transportadora”; <br> (5) Sistema notifica o usuário por email de que o produto foi entregue a transportadora e logo deverá chegar até ele;
(6) Sistema aciona o sistema de pagamento para enviar o valor do pedido para a loja;
(7) Sistema notifica a loja por email de que o valor do pedido foi pago.

<br>

### Fluxos alternativos


[< anterior]() | [próximo >]()

<br><br>


# CDU14 - Atender cliente (suporte)

#### Aluno: Ye Wei Jiang
#### TIA: 41926293

<br>

## Protótipo de tela

Um chat para atender o cliente fica na tela daquela venda específica, que é acessada pela página "Suas vendas"

![Tela de atender cliente (suporte)](../assets/telas/CDU14%20-%20Suporte.png)

<br>

## Fluxograma de negócio
![Fluxo atender cliente]()

---
<br>

## Especificação do caso de uso

<br> | CDU14 - Atender cliente (suporte)
---|---
**Descrição** | Responder mensagens de dúvidas ou problemas do cliente.
**Nível** | Objetivo loja
**Ator principal** | Loja
**Pré-condições** | Loja precisa ser empresa registrada. <br>Loja deve possuir CNPJ e endereço de email.
**Pós-condições** | Conta loja criada. <br>A Loja pode adicionar produtos no catálogo.

<br>

---

### Fluxo principal
Ações da loja | Ações do sistema
--|--
(2) Loja responde a mensagem recebida; | (1) O sistema notifica a loja por email de que recebeu mensagem no sistema; <br> (3) O sistema notifica o cliente.

<br>

### Fluxos alternativos


[< anterior]() | [próximo >]()

<br><br>


# CDU15 - Receber devolução / Devolver dinheiro

#### Aluno: Ye Wei Jiang
#### TIA: 41926293

<br>

## Protótipo de tela

![Tela de devolver dinheiro](../assets/telas/CDU15%20-%20Devolver%20dinheiro.png)

<br>

## Fluxograma de negócio
![Fluxo receber devolução](../assets/casos/15-devolver-dinheiro.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU15 - Receber devolução / Devolver dinheiro
---|---
**Descrição** | Caso em que o cliente deseja devolver o produto recebido.
**Nível** | Objetivo loja
**Ator principal** | Loja
**Pré-condições** | O cliente deve ter solicitado a devolução do produto. <br>O sistema deve ter aceito a solicitação do cliente.
**Pós-condições** | O cliente recebe seu dinheiro de volta. <br>A loja recebe o produto de volta.

<br>

---

### Fluxo principal
Ações da loja | Ações do sistema | Ações do cliente
--|--|--
(2) Loja invoca o sistema de pagamento para devolver o dinheiro; <br> (5) Loja recebe o produto de volta. | (1) Sistema notifica a loja da necessidade de devolução; <br> (3) Sistema de pagamento envia o dinheiro para o cliente; | (4) Cliente envia o produto de volta;

<br>

### Fluxos alternativos
- Cliente não envia o produt ode volta
- Produto devolvido com problemas


[< anterior]() | [próximo >]()

<br><br>


# CDU16 - Denunciar cliente

#### Aluno: Ye Wei Jiang
#### TIA: 41926293

<br>

## Protótipo de tela

![Tela de denunciar cliente](../assets/telas/CDU16%20-%20Denunciar%20cliente.png)

<br>

## Fluxograma de negócio
![Fluxo receber devolução](../assets/casos/16-denunciar-cliente.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU16 - Denunciar cliente
---|---
**Descrição** | Caso, em uma devolução de pedido, a loja devolva a quantia paga pelo <br>cliente mas o cliente não devolva o produto.
**Nível** | Objetivo loja
**Ator principal** | Loja
**Pré-condições** | Em uma situação de devolução de pedido, a loja devolveu o pagamento, <br>mas o cliente não enviou o produto de volta.
**Pós-condições** | O cliente que não seguiu a política é excluído da plataforma. <br>O administrador do sistema reembolsa a loja pelo prejuízo.

<br>

---

### Fluxo principal
Ações da loja | Ações do sistema | Ações do administrdor do sistema
--|--|--
(1) Loja acessa a página do pedido com problema; <br> (2) Loja informa o motivo e denuncia cliente; <br> | (3) Administrador do sistema consulta transportadora para analisar o status da devolução; <br> (4) Administrador do sistema exclui cliente da plataforma; <br> (5) Administrador do sistema aciona o sistema de pagamento para reembolsar loja; | (6) Sistema de pagamento envia o dinheiro do prejuízo para a loja.

<br>

### Fluxos alternativos
- Cliente enviou o pedido de volta

[< anterior]() | [próximo >]()

<br><br>

---

## Administrador do sistema

# CDU17 - Remover cliente

## Fluxograma de negócio
![Fluxo receber devolução](../assets/casos/17-remover-cliente.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU17 - Remover cliente
---|---
**Descrição** | Caso um cliente se demonstre problemático para a plataforma ele <br>poderá ser excluído pelos administradores.
**Nível** | Objetivo administrador do sistema
**Ator principal** | Administrador do sistema
**Pré-condições** | Loja denunciou cliente. <br>Administrador do sistema aprovou denúncia.
**Pós-condições** | Cliente não pode mais comprar no sistema pelo CPF cadastrado.

<br>

---

### Fluxo principal
Ações do administrdor do sistema | <br>
--|--
(1) Administrador do sistema acessa página de controle do sistema; <br> (2) Administrador do sistema busca cliente por CPF; <br> (3) Administrador do sistema remove a conta do cliente do sistema. | 

<br>

### Fluxos alternativos

[< anterior]() | [próximo >]()

<br><br>

# CDU18 - Aprovar criação de conta loja

## Fluxograma de negócio
![Fluxo receber devolução](../assets/casos/18-aprovar-conta-loja.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU18 - Aprovar criação de conta loja
---|---
**Descrição** | Para as lojas criarem conta na plataforma elas precisam ser analisadas <br>e aprovadas pelos administradores.
**Nível** | Objetivo administrador do sistema
**Ator principal** | Administrador do sistema
**Pré-condições** | Loja solicitou filiação ao sistema.
**Pós-condições** | Loja criada. Loja poderá cadastrar e vender produtos.

<br>

---

### Fluxo principal
Ações do administrdor do sistema | <br>
--|--
(1) Administrador do sistema avalia informações da loja; <br> (2) Administrador do sistema aprova criação da conta da loja; <br> (3) Administrador do sistema notifica loja por email sobre a aprovação da conta. | 


<br>

### Fluxos alternativos
- Administrador do sistema não aprova criação da conta

[< anterior]() | [próximo >]()

<br><br>


# CDU19 - Remover loja

## Fluxograma de negócio
![Fluxo receber devolução](../assets/casos/19-remover-loja.jpeg)

---
<br>

## Especificação do caso de uso

<br> | CDU19 - Remover loja
---|---
**Descrição** | Caso uma loja se demonstre problemática para a plataforma ela <br>poderá ser excluída pelos administradores.
**Nível** | Objetivo administrador do sistema
**Ator principal** | Administrador do sistema
**Pré-condições** | Cliente denunciou loja. Administrador do sistema aprovou denúncia.
**Pós-condições** | Loja não pode mais vender no sistema pelo CNPJ e nome cadastrado.

<br>

---

### Fluxo principal
Ações do administrdor do sistema | <br>
--|--
(1) Administrador do sistema acessa página de controle do sistema; <br> (2) Administrador do sistema busca loja por CNPJ; <br>(3) Administrador do sistema remove a conta da loja do sistema; |

<br>

### Fluxos alternativos

[< anterior]() | [próximo >]()

<br><br>