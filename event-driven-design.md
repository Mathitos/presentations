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
![iamgem de exemplo arquitetura do uber](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20201120210648/Uber-System-Design-High-Level-Architecture.png)
