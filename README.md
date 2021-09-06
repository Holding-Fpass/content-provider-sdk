# Content Provider SDK
Package de definições para integração para partners orientado ao conteúdo gerado e disponível na plataforma Fpass.

## Responsability
Criar meio de acesso a conteúdos que possam ser acessados e utiliados por parceiros (Partners) que são gerado na plataforma (Fpass).

## Overview User
![Content User](https://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/Holding-Fpass/content-provider-sdk/main/uml/content-user-v2.0.0.iuml)

### User
A criação de um novo usuário deverá utilizar os campos descritos na documentação da [Content Provider OpenAPI](https://raw.githubusercontent.com/Holding-Fpass/content-provider-sdk/main/content-provider-openapi.yml).

Um id externo (externalId) poderá ser informado no campo data com a finalidade de ser um identificador do partner na plataforma Fpass.

## Overview Display
![Content Display](https://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/Holding-Fpass/content-provider-sdk/main/uml/content-display-v2.0.0.iuml)

### Display
Para obter dados de exibição de conteúdos e listagens devem ser utilizados os metodos de Display encontrados na Content Provider OpenAPI.

### Authentication
Deverão ser utilidados os seguintes métodos de autenticação:
- API Key: Para uso nos endpoints de criação, crendencialmento e recuperação de acesso do usuário.
- Bearer Token: Para uso de demais endpoints

### Autorization Header Verification / JWT Verification
Verificação do _header_ _Autorization_ da _Request_ onde o _Bearer_ contêm um JWT.
- Signing default: RS256