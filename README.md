# Spring Data JPA - Relacionamento de Entidades


## [datajpa-relacionamento-entidades]

:desktop_computer: :keyboard: :computer_mouse: :coffee:

### Breve Relato :bulb:

>Esta será uma **API** para um **data base** com as *tabelas* ***city, zipcode, author, book e category,*** no qual utilizarei anotações da *Spring Data JPA*.



## :point_right: Tecnologias empregadas
> - Linguagem Java 11.
> - Spring Boot / Spring Web /Spring Data JPA.
> - Banco de dados H2 Database.
> - Lombok.
> - IDE Eclipse.
>



## 💎 Diagrama entidade relacionamento.

![diagram-authorl-book](https://github.com/pliniopereira10/images/blob/c4d528fdfc28413e1988f6e39d3146bac72ec0ca/diagram-images/diagram-author-book.png)


### OneToOne - OneToMany - ManyToOne - ManyToMany

| City e Zipcode | Author e Zipcode | Author e Book | Book e Category |
| :------------- | ---------------- | ------------- | --------------- |
| OneToOne       | OneToMany        | ManyToMany    | ManyToOne       |
| Unidirecional  | Unidirecional    | Bidirecional  | Bidirecional    |


### @JoinColumn vc MappedBy

- A anotação ***@JoinColumn*** indica que esta entidade é proprietária do relacionamento.
- O atributo ***MappedBy*** indica que essa entidade é o inverso do relacionamento.




##  ![database random](https://emojis.slackmojis.com/emojis/images/1643514101/596/database.png?1643514101) Configurações

- `application.properties`

    ```properties
    spring.h2.console.enabled=true
    spring.h2.console.path=/h2-console
    
    spring.datasource.driverClassName=org.h2.Driver
    spring.datasource.url=jdbc:h2:mem:testdb
    spring.datasource.username=sa
    spring.datasource.password=
    
    spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
    spring.jpa.show-sql=true
    spring.jpa.open-in-view=false
    ```
