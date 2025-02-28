# API RESTFUL WEB FORNECEDORES

Este projeto é uma API RESTful desenvolvida em Spring Boot para gerenciar fornecedores. Ele inclui funcionalidades para listar, buscar, salvar, 
atualizar e deletar fornecedores.
O projeto utiliza SQLite como banco de dados e Thymeleaf para a interface web.

## Tecnologias Utilizadas

- **Spring Boot**: Framework para desenvolvimento de aplicações Java.
- **SQLite**: Banco de dados leve e embutido. Arquivo fornecedores.DB.
- **Thymeleaf**: Motor de templates para renderização de páginas web.
- **Hibernate**: ORM (Object-Relational Mapping) para mapeamento de objetos Java para tabelas do banco de dados.

## Estrutura do Projeto

O projeto está organizado da seguinte forma:

- **Config**: Contém a configuração do dialeto SQLite para o Hibernate.
- **Controller**: Contém os controladores para a API RESTful e a interface web.
- **Entity**: Contém a entidade `Fornecedor` que representa a tabela no banco de dados.
- **Repository**: Contém a interface `FornecedorRepository` para operações de banco de dados.
- **Service**: Contém a classe `FornecedorService` que implementa a lógica de negócio.

## Classes Principais

### SQLiteDialect

Esta classe estende o `Dialect` do Hibernate para suportar o SQLite. Ela define os tipos de colunas e funções específicas do SQLite.

### ApiFornecedorController

Controlador RESTful para gerenciar fornecedores. Expõe endpoints para listar, buscar, salvar, atualizar e deletar fornecedores.

```java
@RestController
@RequestMapping("/api/fornecedores")
public class ApiFornecedorController {
    // Métodos para manipulação de fornecedores
}
```

### WebFornecedorController

Controlador para a interface web. Renderiza páginas HTML usando Thymeleaf.

```java
@Controller
@RequestMapping("/fornecedores")
public class WebFornecedorController {
    // Métodos para renderização de páginas web
}
```

### Fornecedor

Entidade que representa um fornecedor no banco de dados.

```java
@Entity
@Table(name = "FORNECEDORES")
public class Fornecedor {
    // Atributos e métodos getters/setters
}
```

### FornecedorRepository

Interface que estende `JpaRepository` para operações de banco de dados.

```java
public interface FornecedorRepository extends JpaRepository<Fornecedor, Long> {
}
```

### FornecedorService

Classe de serviço que implementa a lógica de negócio para manipulação de fornecedores.

```java
@Service
public class FornecedorService {
    // Métodos para manipulação de fornecedores
}
```

## Configuração do Projeto

### Dependências

O projeto utiliza as seguintes dependências principais:

- `spring-boot-starter-data-jpa`: Para integração com JPA e Hibernate.
- `spring-boot-starter-thymeleaf`: Para renderização de páginas web.
- `spring-boot-starter-web`: Para desenvolvimento de aplicações web.
- `sqlite-jdbc`: Driver JDBC para SQLite.

### Arquivo `pom.xml`

O arquivo `pom.xml` contém todas as dependências e configurações do projeto.

```xml
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-thymeleaf</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
        <groupId>org.xerial</groupId>
        <artifactId>sqlite-jdbc</artifactId>
    </dependency>
</dependencies>
```

## Como Executar o Projeto

1. **Acesse a aplicação**:
   - API RESTful: `http://localhost:8080/api/fornecedores`
   - Interface Web: `http://localhost:8080/fornecedores`

### Explicação do Conteúdo:

1. **Título e Descrição**: Fornece uma visão geral do projeto.
2. **Tecnologias Utilizadas**: Lista as principais tecnologias e frameworks usados.
3. **Estrutura do Projeto**: Descreve a organização das pastas e classes.
4. **Classes Principais**: Detalha as principais classes do projeto, incluindo snippets de código.
5. **Configuração do Projeto**: Explica as dependências e o arquivo `pom.xml`.
6. **Como Executar o Projeto**: Fornece instruções passo a passo para rodar o projeto.
7. **Contribuição**: Informa como contribuir para o projeto.
8. **Licença**: Indica a licença sob a qual o projeto está disponível.
