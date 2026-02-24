# Projeto Mongo
[![NPM](https://img.shields.io/npm/l/react)](https://github.com/CassioMM/workshop-springboot4-jpa/blob/main/LICENSE) 

# Sobre o projeto
Este projeto é uma API REST desenvolvida em Java com Spring Boot integrada ao MongoDB, criada como parte de um curso sobre banco de dados NoSQL e desenvolvimento de APIs com Spring. O foco principal é aplicar conceitos como persistência de dados em banco orientado a documentos, consultas com critérios de texto e data, e relacionamento entre entidades.

## Tecnologias Utilizadas
- Java 25
- Spring Boot
- Spring Data MongoDB
- MongoDB (NoSQL)
- Maven
- Postman (para testes)

## Modelo conceitual
<img width="861" height="241" alt="image" src="https://github.com/user-attachments/assets/9b72926b-cce6-44b4-84ba-9f4dcda9b3eb" />

## Layout Postman
<img width="676" height="707" alt="image" src="https://github.com/user-attachments/assets/cb875d52-6207-4c58-a733-9f36ef425467" />

---

## Arquitetura baseada em camadas:

O projeto segue a arquitetura em camadas:

- domain/ → Entidades (User, Post, CommentDTO)

- repositories/ → Interfaces MongoRepository

- resources/ → Controllers (endpoints REST)

- config/ → Configurações e instâncias iniciais


## Controllers (Endpoints da API)

Os controllers estão localizados no pacote:

```com.cassiom.workshopmongo.repository```

### User
| Método | Rota          | Descrição               |
| ------ | ------------- | ----------------------- |
| GET    | `/users`      | Lista todos os usuários |
| GET    | `/users/{id}` | Busca usuário por ID    |
| POST   | `/users`      | Cria um novo usuário    |
| DELETE | `/users/{id}` | Remove usuário          |

### Post
| Método | Rota                                                               | Descrição            |
| ------ | ------------------------------------------------------------------ | -------------------- |
| GET    | `/posts`                                                           | Lista todos os posts |
| GET    | `/posts/{id}`                                                      | Busca post por ID    |
| GET    | `/posts/titlesearch?text=abc`                                      | Busca por título     |
| GET    | `/posts/fullsearch?text=abc&minDate=yyyy-MM-dd&maxDate=yyyy-MM-dd` | Busca completa       |
| DELETE | `/posts/{id}`                                                      | Remove post          |


##  Como Executar

### Pré-requisitos

- Java 17+
- MongoDB rodando na porta padrão (27017)
- Maven

### Passos

Clone o repositório:

```bash
git clone https://github.com/CassioMM/curso-projeto-mongo.git
cd curso-projeto-mongo

Execute a aplicação:
./mvnw spring-boot:run

A API estará disponível em:
http://localhost:8080
```
# Autor

Cássio Montenegro

www.linkedin.com/in/cássio-montenegro-marques

# Dedicatoria

[DevSuperior](https://devsuperior.com "Site da DevSuperior")
