---
marp: true
author: Matheus Anzzulin
theme: payfy-theme
size: 4:3
footer: " "
---
<!-- _class: lead -->
# Blockchain principios
### por Matheus Anzzulin
---

# DDD

### Oque é
  - Analise do software top down
  - Foco no problema a ser resolvido e não na tecnologia
  - Faz modelos de dados baseado no dominio do negócio e o software tem que se adaptar a ele.

---
# DDD
*(Oque é top down)*

Contexto -> Loja de bicicleta

Modelo -> Bicicleta, Pedido, Cliente, Vendedor

Linguagem unica -> Ciclista, Peças

Sub Contextos -> Venda, Aluguel

---

# Elixir
### DDD em Elixir

- Contextos são modulos dedicados que expoem e agrupam funcionalidades relacionadas

- Projetos em phoenix já vem com a ideia de contextos "out of the box"

---

## Exemplo de contextos definidos
- [Lib Boundary](https://github.com/sasa1977/boundary)

---

# Behaviour Driven Development
