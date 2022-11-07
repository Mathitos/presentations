---
marp: true
author: Matheus Anzzulin
theme: payfy-theme
size: 4:3
footer: " "
---
<!-- _class: lead -->
# Resumo Banco de dados
### por Matheus Anzzulin
---
# Banco de dados Relacional
É um banco de dados modelado para expressar e reconhecer conexões entre registros.
São diversas tabelas que podem ou não se relacionar entre si.
Cada tabela tem colunas com nomes, e linhas com registros.

| Id | Nome | Cidade |
| ---| --- | ---|
| 1 | Matheus | Porto Alegre|
| 2 | Carolina | Pelotas |

--

| Id | Github | UserId |
| ---| --- | ---|
| 1 | tavarescarolina | 2|
| 2 | Mathitos | 1|

---

# Banco de dados não relacional

Tem outros focos que não a modelagem de dados focado no relacionamento entre esquemas.
```
{
  "1": {"nome": "Matheus", "darkmode": true},
  "2": {"nome": "Carolina", "notifications": false}
}
```

---
# ACID
### **(Atomicidade, Consistencia, Isolação e Durabilidade)**
São Propriedades de uma transação de um banco de dados relacional que garantem a validade dos dados.

---
# ACID
## Atomicidade
Transações podem ser compostas de diversas declarações, aonde deve-se garantir que ou todas declarações são bem sucedidas ou todas falham.
```
Exemplo:
Adiciona na tabela de compras uma compra na steam de 20 reais
Subtrai o saldo atual do usuário na tabela de saldos
```
---
# ACID
## Consistencia
Transações só podem ser bem sucedidas se levarem o bando de dados de um estado consistente a outro. Isso que dizer que só são salvas transações que respeitem todas as regras definidas no banco.

```
Exemplo:
Banco de dados é modelado para que o saldo de um usuário nunca deve ser negativo.
Um transação de compra de 10 reais ,
para um usuário com saldo de 20 reais é bem sucedida e salva no banco.
Um transação de compra de 20 reais,
 para um usuário com saldo de 10 reais não é bem sucedida e logo não é
 salva no banco pois o novo estado viola uma regra do mesmo.
```

---
# ACID
## Isolação
---
# ACID
## Durabilidade

---

# Structure Query Language

### Linguagem focada em CRUD de baco de dados

---

CREATE DATABASE presentation;
USE presentation;

CREATE TABLE attendees (
  id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(255),
  age INT,
);

ALTER TABLE attendees ADD is_present BOOLEAN DEFAULT 'true' NOT NULL;

CREATE TABLE locations (
  id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(255),
  PRIMARY KEY(id)
);
DROP TABLE locations;

CREATE TABLE questions (
  id INT NOT NULL AUTO_INCREMENT,
  question VARCHAR(255),
  is_answered BOOLEAN DEFAULT 'false',
  attendee_id INT NOT NULL,
  PRIMARY KEY(id),
  FOREIGN KEY (attendee_id) REFERENCES attendees(id)
);

INSERT INTO attendees (name, is_present) VALUES ('Matheus Anzzulin', 'true');
INSERT INTO attendees (name, age, is_present) VALUES ('Anonimo', 20, 'true');

INSERT INTO attendees (name, is_present) VALUES
('Carolina Tavares', 'true'),
('Lucas Brasil', 'true'),
('Guilherme Schweizer', 'true');

SELECT * FROM attendees;
SELECT name AS 'nome', age AS 'idade' FROM attendees;

INSERT INTO attendees (name, is_present) VALUES ('Ariele Cassaroti', 'false');
SELECT * FROM attendees WHERE is_present;

SELECT * from attendees WHERE name LIKE '%athe';

INSERT INTO questions (question, is_answered, attendee_id) VALUES ('como atualizar um registro?', 'false', 1);

UPDATE questions WHERE id = 1 SET is_answered = 'true';
SELECT * FROM questions;

SELECT * FROM attendees WHERE age IS NULL;
UPDATE attendees WHERE age IS NULL SET age = 10;

INSERT INTO questions (question, is_answered, attendee_id) VALUES ('como usar a parte relacional do banco com SQL?', 'false', 1);

SELECT * FROM attendees
INNER JOIN questions ON attendees.id = questions.attendee_id;

SELECT * FROM attendees
LEFT JOIN questions ON attendees.id = questions.attendee_id;

SELECT * FROM attendees
LEFT JOIN questions ON attendees.id = questions.attendee_id
WHERE NOT questions.is_answered;

SELECT * FROM attendees
RIGHT JOIN questions ON attendees.id = questions.attendee_id;

SELECT AVG(age) from attendees;
SELECT AVG(is_present) from attendees;

SELECT attendee_id, COUNT (id) FROM questions GROUP_BY attendee_id;

SELECT attendees.name, COUNT (questions.id) FROM attendees
LEFT JOIN questions ON attendees.id = questions.attendee_id
GROUP_BY questions.attendee_id;

SELECT a.name as 'nome do participante', COUNT (q.id) as 'numero de perguntas' FROM attendees AS a
LEFT JOIN questions AS q ON a.id = q.attendee_id
GROUP_BY q.attendee_id;
