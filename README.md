# API RESTful - Sistema de Gerenciamento de Produtos

Bem-vindo à API RESTful para o sistema de gerenciamento de produtos. Esta API segue os princípios fundamentais da arquitetura REST e inclui suporte ao HATEOAS (Hypermedia as the Engine of Application State).

## Pré-requisitos
Certifique-se de ter o ambiente configurado com Java e as dependências do Spring Boot. Além disso, é recomendável ter um banco de dados configurado.

## Padrões RESTful Implementados
A API segue os pilares fundamentais da arquitetura REST:

1. **Stateless:** Cada requisição do cliente para o servidor deve conter todas as informações necessárias para entender e processar a requisição. O servidor não deve armazenar informações do estado do cliente entre requisições.

2. **Uniform Interface:** A interface é simplificada e consistente para todas as interações. Isso inclui a utilização de verbos HTTP padronizados (GET, POST, PUT, DELETE), URIs significativas e a representação de recursos no formato JSON.

3. **Client-Server:** A separação entre cliente e servidor permite a evolução independente de ambas as partes, facilitando a escalabilidade e a manutenção.

4. **Cacheability:** As respostas devem ser explicitamente marcadas como cacheáveis ou não-cacheáveis. Isso melhora a eficiência e a escalabilidade.

5. **Layered System:** A arquitetura pode ser composta por camadas hierárquicas, facilitando a escalabilidade e a manutenção.

## HATEOAS (Hypermedia as the Engine of Application State)
A API implementa o HATEOAS. Isso significa que as respostas incluem links para recursos relacionados, permitindo que o cliente navegue pela aplicação de maneira dinâmica.

Por exemplo:
- Ao obter a lista de produtos, cada produto possui links para visualizar detalhes específicos desse produto.
- Ao visualizar os detalhes de um produto, há um link para retornar à lista completa de produtos.

## Endpoints Disponíveis

- **POST /products:** Cria um novo produto.
- **GET /products:** Retorna a lista completa de produtos.
- **GET /products/{id}:** Retorna os detalhes de um produto específico.
- **PUT /products/{id}:** Atualiza as informações de um produto.
- **DELETE /products/{id}:** Exclui um produto.
