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


---

# Banco de dados não relacional

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

ALTER TABLE attendees ADD is_present BOOLEAN DEFAULT TRUE NOT NULL;

CREATE TABLE locations (
  id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(255),
  PRIMARY KEY(id)
);
DROP TABLE locations;

CREATE TABLE questions (
  id INT NOT NULL AUTO_INCREMENT,
  question VARCHAR(255),
  is_answered BOOLEAN DEFAULT FALSE,
  attendee_id INT NOT NULL,
  PRIMARY KEY(id),
  FOREIGN KEY (attendee_id) REFERENCES attendees(id)
);

INSERT INTO attendees (name, is_present) VALUES ('Matheus Anzzulin', TRUE);
INSERT INTO attendees (name, age, is_present) VALUES ('Anonimo', 20, TRUE);

INSERT INTO attendees (name, is_present) VALUES
('Carolina Tavares', TRUE),
('Lucas Brasil', TRUE),
('Guilherme Schweizer', TRUE);

SELECT * FROM attendees;
SELECT name AS 'nome', age AS 'idade' FROM attendees;

INSERT INTO attendees (name, is_present) VALUES ('Ariele Cassaroti', FALSE);
SELECT * FROM attendees WHERE is_present = TRUE;

SELECT * from attendees WHERE name LIKE '%athe';

INSERT INTO questions (question, is_answered, attendee_id) VALUES ('como atualizar um registro?', false, 1);

UPDATE questions WHERE id = 1 SET is_answered = TRUE;
SELECT * FROM questions;

SELECT * FROM attendees WHERE age IS NULL;
UPDATE attendees WHERE age IS NULL SET age = 10;

SELECT * FROM attendees
INNER JOIN questions ON attendees.id = questions.attendee_id;

SELECT * FROM attendees
LEFT JOIN questions ON attendees.id = questions.attendee_id;

SELECT * FROM attendees
RIGHT JOIN questions ON attendees.id = questions.attendee_id;
