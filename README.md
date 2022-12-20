# Sprinp Data JPA - Relacionamento de Entidades

Esta será uma **API** para um **data base** com as *tabelas* ***city, zipcode, author, book e category,*** no qual utilizarei anotações da *Spring Data JPA*.

## OneToOne - OneToMany - ManyToOne - ManyToMany

| City e Zipcode | Author e Zipcode | Author e Book | Book e Category |
| :------------- | ---------------- | ------------- | --------------- |
| OneToOne       | OneToMany        | ManyToMany    | ManyToOne       |
| Unidirecional  | Unidirecional    | Bidirecional  | Bidirecional    |

## @JoinColumn vc MappedBy

- A anotação ***@JoinColumn*** indica que esta entidade é proprietária do relacionamento.
- O atributo ***MappedBy*** indica que essa entidade é o inverso do relacionamento.

## Tecnologias

- Spring Web

- Spring Data JPA

- H2 Database

- Lombok

## Configurações 

- `application.properties`

        spring.h2.console.enabled=true
        spring.h2.console.path=/h2-console
        
        spring.datasource.driverClassName=org.h2.Driver
        spring.datasource.url=jdbc:h2:mem:testdb
        spring.datasource.username=sa
        spring.datasource.password=
        
        spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
        spring.jpa.show-sql=true
        spring.jpa.open-in-view=false

## Entidades

- City
- Zipcode
- Author
- Book
- Category
