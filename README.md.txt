- Projeto Azure - Rede Virtual com NSG e IP Público

Este projeto cria uma infraestrutura no Azure usando uma Rede Virtual, Sub-rede, Network Security Group (NSG) e um IP Público, usando ARM Template exportado do Portal do Azure, com o objetivo de praticar os conceitos de redes virtuais e segurança no Azure, bem como um template para futuros projetos.

- Recursos Criados

1. Rede Virtual (VNet)
2. Sub-rede
3. Network Security Group (nsg) com regras de entrada:
 3.1 - SSH (Porta 22)
 3.2 - HTTP (Porta 80)
 3.3 - HTTPS (Portal 443)
4. Endereço de IP Público associado à Sub-rede.

- Arquitetura

+----------------------------+
| Rede Virtual |
| (VNet) |
| |
| +----------------------+ |
| | Sub-rede | |
| | | |
| | +----------------+ | |
| | | NSG | | |
| | +----------------+ | |
| | | |
| +----------------------+ |
| |
+----------------------------+
|
v
IP Público (IPv4)

- Prints do Portal do Azure:

Dashboard do Azure
![Dashboard] (print/dashboard.png)

Criar Grupo de Recursos
![Projeto-arm] (print/projeto-arm.png)
![Projeto-arm] (print/projeto-arm criado.png)

Rede Virtual
![VNet] (print/vnet.png)

Sub-rede
![Sub-rede] (print/sub-rede.png)

Network Security Group (NSG)
![NSG](print/NSG.png)
![regrasnsg] (print/regrasnsg.png)
![criandoregrasnsg] (print/criandoregrasnsg.png)
![subrede] (print/subrede.png)

IP Público
![ip-publico-projeto] (print/ip-publico-projeto.png)


- Como usar: Passo a passo
1. Acesse o Portal do Azure Estúdio
[https://azure.microsoft.com]

2. Crie uma conta usando: e-mail, nº de telefone e cartão de crédito. (Considerando que não existe nenhuma assinatura válida).

3. Finalize o cadastro e acesse o Portal do Azure [https://portal.azure.com]

4. No Dashboard do Azure, use o Menu à esquerda ou a barra de pesquisa para buscar recursos. 

5. Criando um novo Recurso:

  Na barra de pesquisa digite: Grupo de Recurso 
  Clique em "+ Criar" no topo
  Preencha: Assinatura (válida), Grupo de recursos (nome do recurso a ser criado), Região 
  Clique em Revisar + Criar
  Depois clique em Criar
  Grupo criado com sucesso!

6. Criando a Rede Virtual e Sub-Rede

  Na barra de pesquisa digite: Rede Virtual
  Clique em "+ Criar"
  Preencha: Assinatura (válida), Grupo de recursos (recurso criado), Nome (nome da rede virtual), Região
  Na mesma página em Endereços IP: Editar sub-rede - Nome(subnet-projeto), Prefixo (10.0.1.0/24)
  Clique em Revisar + Criar
  Depois clique em Criar
  Rede criada com sucesso!

7. Criando o Network Security Group (NSG)

  Define as regras de entrada e saída para proteger a VNet.
  Na barra de pesquisa digite: Grupo de Segurança da Rede
  Clique em "+ Criar"
  Preencha: Assinatura (válida), Grupo de recursos (recurso criado), Nome (nome do grupo de segurança), Região
  Clique em Revisar + Criar
  Depois clique em Criar
  Grupo de Segurança criado com sucesso!
  Após a criação, vá para ele e clique em Regras de segurança de entrada. (Configurações -> Regras de Segurança de Entrada)
  Clique em "+ Adicionar"
  Crie as regras e salve cada uma.
  Vá em Configurações -> Sub-redes e clique em associar.
  Selecione Rede Virtual (nome rede criada) e Sub-rede (nome sub criada)
  Clique em OK
  A sub-rede está protegida pelo NSG.

8. Criando um IP Público

  Na barra de pesquisa digite: Endereço de IP público
  Clique em "+ Criar"
  Preencha: Assinatura (válida), Grupo de recursos (recurso criado), Nome (ip-publico-projeto), Região
  Depois clique em Criar
  IP Público criado com sucesso!

- Tecnologias Usadas

 1. [Microsoft Azure](https://azure.microsoft.com/)
 2. [ARM Templates](https://learn.microsoft.com/azure/azure-resource-manager/templates/overview)
 3. Markdown para documentação

- Autor

 Dannuza Martins Cardoso Silva
 endereço GITHUB
 


