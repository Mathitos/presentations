---
marp: true
theme: payfy-theme
footer: " "
---
<!-- _class: lead -->
# Persistindo dados entre janelas no React
### por Matheus Anzzulin
---
## Primeiro vamos começar criando um boilerplate
##### commit #23a4224
Um Form simples para compartilhar dados

---
## Syncronizar janelas usando o Local Storage
##### commit #334d633
Para manter o estado salvo
Devemos:
- salvar dados no local storage no evento de submit
- limpar os dados no logout
- buscar dados salvo na inicialização do componente

---
## Syncronizar janelas usando o Local Storage
##### commit #43198b0
Devemos:
- salvar dados no local storage no evento de submit
- limpar os dados no logout
- buscar dados salvo na inicialização do componente
