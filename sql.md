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
  name VARCHAR(255),
  age INT,
);
ALTER TABLE attendees ADD is_present BOOLEAN NOT NULL;