# 📌 Projeto Final – Capacitação Interna - APITest: Da Requisição à Confiança

## 🎯 Objetivo

Este projeto foi desenvolvido como avaliação final da capacitação **"APITest: Da Requisição à Confiança"**, promovida pela Minsait - comunidade de testes Testing Hub. O objetivo é demonstrar na prática as habilidades de planejamento, execução e automação de testes de API utilizando o Postman.

A coleção de testes implementa um fluxo End-to-End (E2E) completo e dinâmico, cobrindo todo o ciclo de vida (CRUD) de um recurso na [Simple Books API](https://simple-books-api.click).

---

## 📄 Documentação da API (Swagger)

A especificação completa da API, no formato OpenAPI 3.0, está disponível no arquivo `Swagger Capacitação.yaml`. Para visualizar a documentação de forma interativa:

1.  Abra o arquivo `Swagger Capacitação.yaml` e copie todo o seu conteúdo.
2.  Acesse o **[Swagger Editor](https://editor.swagger.io/)**.
3.  Cole o conteúdo no editor online. A documentação interativa será renderizada, permitindo a consulta de todos os endpoints, parâmetros e respostas.

---

## 📋 Cenários Automatizados

O fluxo principal, executado através do Collection Runner, valida a seguinte sequência de operações:

1.  **`POST Registrar cliente na API`**: Gera dados aleatórios, registra um novo cliente e extrai o `accessToken` para uso nas requisições autenticadas.
2.  **`GET Retornar uma lista de livros`**: Obtém a lista de livros disponíveis e extrai o `bookId` de um livro.
3.  **`POST Enviar um novo pedido`**: Utiliza o `accessToken` e o `bookId` para criar um novo pedido e extrai o `orderId`.
4.  **`GET Listar pedido criado`**: Busca o pedido recém-criado e valida seu conteúdo.
5.  **`PATCH Atualizar um pedido`**: Altera o nome do cliente no pedido existente.
6.  **`DELETE Excluir um pedido existente`**: Exclui o pedido criado e valida o sucesso da operação.
7.  **(Validação de Exclusão)** Uma requisição `GET` subsequente ao pedido excluído é executada para confirmar que ele não é mais encontrado (espera-se um erro `404`).

*As demais requisições na coleção servem para testes manuais e exploratórios.*

---

## 🚀 Como Executar os Testes

Para executar esta coleção, siga os passos abaixo:

### 1. Pré-requisitos
*   Ter a versão mais recente do [Postman](https://www.postman.com/downloads/) instalada.

### 2. Importar a Coleção e o Ambiente

1.  Abra o Postman.
2.  Clique no botão **`Import`**.
3.  Arraste e solte os dois arquivos `.json` deste repositório:
    *   `Simple_Books_API_Collection.postman_collection.json`
    *   `Simple_Books_API.postman_environment.json`
4.  Confirme a importação.

### 3. Executar os Testes com o Collection Runner

1.  No painel esquerdo, encontre a coleção importada.
2.  Clique nos três pontinhos (`...`) ao lado do nome da coleção e selecione **`Run collection`**.
3.  Na janela do Runner, **ative o ambiente** `Simple Books API - Env`.
4.  Organize as requisições na ordem correta do fluxo E2E, se necessário.
5.  Clique no botão azul **`Run [Nome da Coleção]`**.

Ao final da execução, o resumo do Runner exibirá o resultado de todos os testes, demonstrando o sucesso do fluxo automatizado.

---
## ✍️ Autor
Desenvolvido por **Bruna Amaral** como projeto final da capacitação *APITest: Da Requisição à Confiança*.
