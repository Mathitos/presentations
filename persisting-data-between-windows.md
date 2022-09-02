---
marp: true
author: Matheus Anzzulin
theme: payfy-theme
size: 4:3
footer: " "
---
<!-- _class: lead -->
# Persistindo dados entre janelas no React
### por Matheus Anzzulin
---

## Repo com exeplo prático
https://github.com/Mathitos/local-storage-exemple

---
## Primeiro vamos começar criando um boilerplate
##### commit #23a4224
Um Form simples para compartilhar dados

---
## Sincronizar janelas usando o Local Storage
##### commit #334d633
Para manter o estado salvo, devemos:
- salvar dados no local storage no evento de submit
- limpar os dados no logout
- buscar dados salvo na inicialização do componente

---
## Sincronizar janelas usando o Local Storage
##### commit #43198b0
para manter as janelas sincronizadas, devemos:
- subscrever o app a eventos do localstorage
