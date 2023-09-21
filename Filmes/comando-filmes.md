# Comandos SQL - Referência

### Criar banco de dados

```sql

CREATE DATABASE filmes CHARACTER SET utf8mb4;

```

### Criar a tabela de Generos

```sql

CREATE TABLE Generos (
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(45) NOT NULL
    
)

```

### Criar a tabela Filmes

```sql

CREATE TABLE Filmes (
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(45) NOT NULL,
    lançamento YEAR(4)

)

```

### Adicionar campo/colunas em uma tabela

```sql

ALTER TABLE filmes ADD genero_id INT NOT NULL
AFTER lançamento;

```

### Chave estrangeira

```sql

ALTER TABLE produtos
    # CONSTRAINT é uma restrição definida no relacionamento
    ADD CONSTRAINT fk_produtos_fabricantes

    # A chave estrangeira deve fazer referencia a chave primaria
    FOREIGN KEY(fabricante_id) REFERENCES fabricantes(id)

```

### Generos

```sql

INSERT INTO Generos (Nome)
VALUES('Ação'),('Drama'),('Crime'),('Romance'),('Suspense');

```

### Filmes

```sql


INSERT INTO filmes (nome, lançamento, genero_id)
VALUES('Fight Club', 1999, 3);

INSERT INTO filmes (nome, lançamento, genero_id)
VALUES('Baby Driver', 2017, 1);

INSERT INTO filmes (nome, lançamento, genero_id)
VALUES('Scott Pilgrim vs. the world', 2010, 4);

INSERT INTO filmes (nome, lançamento, genero_id)
VALUES('The Dark Knight', 2008, 5);

INSERT INTO filmes (nome, lançamento, genero_id)
VALUES('Oppenheimer', 2023, 2);


```