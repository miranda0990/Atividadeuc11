LeiloesTDSsat - sistema de leilões

##  Autora

**Nome:** Lívia Miranda 
**Instituição:** Senac - RS

> Um projeto de software para gerenciamento de uma casa de leilões, para cadastro de produtos e visualização de produtos.

## Tecnologias:
- **Cadastro de produtos**: Cadastro de nome e valor de produtos;
- **Listagem (ArrayList)**: Consulta de produtos cadastrados no banco de dados com o uso da estrutura ArrayList;
- **Persistência de dados**: Conexão com banco de daod MySQL;
- **Tabela de consulta**: Tabela integrada ao sistema, mostrando os produtos cadastrados junto com seu valor e status no estoque

## Estrutura do projeto:
> ConectaDAO.java: Classe com o método de conexão entre projeto e banco de dados;
> ProdutosDAO.java: Classe para os métodos de cadastro de produtos e listagem de produtos;
> ProdutosDTO.java: Classe para a declaração de variáveis da tabela;
> cadastroVIEW.java: Interface principal para inserção de dados;
> listagemVIEW.java: Interface para a consulta de dados ja cadastrados;

## Técnologias utilizadas:
- **Linguagem**: Java;
- **Ambiente de desenvolvimento**: Apache NetBeans;
- **Base de dados**: MySQL;
- **Conector**: Connector/j

## Execução do projeto:
**1- Pré-requisitos**:
> Java JDK 8 ou superior;
> IDE NetBeans;
> Mysql Server ativo;

 **2- Configuração do banco de dados**:
 Abra seu terminal MySQL e utlize esses comandos para a criação do banco de dados:
 CREATE DATABASE uc11;
 USE uc11;
 CREATE TABLE produtos(
 id int not null auto_increment,
 Nome VARCHAR (100),
 Valor int,
 Status VARCHAR(100),
 PRIMARY KEY (id)
 );

**3- Configuração Driver JDBC**:
> Baixe o conector java em: https://www.mysql.com/products/connector/
> No NetBeans, vá ate a aba projetos e escolha o projeto que estamos trabalhando;
> Clique com o botão direito em Libraries e em Add JAR/Folder;
> Selecione o conector em seu arquivos e clique em Abrir

**4- Ajuste de conexão**:
Abra o arquivo ConectaDAO.java e altere a seguinte linha:
> conn = DriverManager.getConnection("jdbc:mysql://localhost/uc11/root/yourpassword");
> root: Seu usuário
> yourpassword: Sua senha do MySQL

**5- Execução**:
> Clique em "Run file" ou use o atalho F5;
> Adicione alguns item para testar;
> Clique no botão que leva a tabela para verificar se os itens estão sendo salvos corretamente

 
##
##
