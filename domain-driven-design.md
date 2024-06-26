---
marp: true
author: Matheus Anzzulin
theme: payfy-theme
size: 4:3
footer: " "
---
<!-- _class: lead -->
# Domain Driven Design
### por Matheus Anzzulin
---
## Disclaimer
Apresentação inspirada na talk:
[*ElixirConf 2020 - Japa Swadia - Domain-Driven Design with Elixir*](https://www.youtube.com/watch?v=fx3BmpzitUg)

[*Real World Example with Elixir Protocol*](https://dev.to/edisonywh/real-world-example-with-elixir-protocol-57ec)
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
