---
marp: true
author: Matheus Anzzulin
theme: payfy-theme
size: 4:3
footer: " "
---
<!-- _class: lead -->
# Singleton
### por Matheus Anzzulin

---
# Pontos Chave
- Controle mais estrito sobre o estado do sistema
- Inicialização unica

---
Quanto uma parte do sistema deve ter apenas uma instancia disponivel para todos os clientes, por exemplo, um unico banco de dados compartilhado por diferentes partes do sistema.
![imagem de exemplo arquitetura de pagamentos com cartão](
https://refactoring.guru/images/patterns/content/singleton/singleton-comic-1-en.png?id=157509c5693a657ba465c7a9d58a7c25)
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
