---
marp: true
author: Matheus Anzzulin
theme: payfy-theme
size: 4:3
footer: " "
---
<!-- _class: lead -->
# Event Driven Design
### por Matheus Anzzulin

---
# Pontos Chave
- Design Pattern arquitetural
- Comunicação Assíncrona

---
# Problema

- Comunicação Síncrona
- Necessidade de sistemas distribuidos
- Não bloquear sistemas chaves com fluxos complexos

---
# Como funciona

Publishers
&darr;

Event Bus
&darr;

Broker
&darr;

Broadcast
&darr;

Consumers

---
# Exemplo (Uber)
![imagem de exemplo arquitetura do uber](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20201120210648/Uber-System-Design-High-Level-Architecture.png)

---
# Exemplo (Pagamentos com cartão)
![imagem de exemplo arquitetura de pagamentos com cartão](
https://marvel-b1-cdn.bc0a.com/f00000000017219/documents.trendmicro.com/images/tex/articles/cloud-pos.jpg)
