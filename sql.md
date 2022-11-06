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

SELECT * FROM attendees;
SELECT name FROM attendees;
