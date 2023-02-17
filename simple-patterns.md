---
marp: true
author: Matheus Anzzulin
theme: payfy-theme
size: 4:3
footer: " "
---
<!-- _class: lead -->
# Padrões de design em elixir
### por Matheus Anzzulin
---

# Factory
Segundo o GOF (Group Of Four) o padrão Factory Method é: “Um padrão que define uma interface para criar um objeto, mas permite às classes decidirem qual classe instanciar. O Factory Method permite a uma classe deferir a instanciação para subclasses”.

---
### Exemplo:

```
apps/payfy/test/support/factory.ex


```

```
apps/adapters/test/adapters/swap/account_processor_test.exs

user = PayfyFactory.insert!(:user, status: :activated)
...

user = PayfyFactory.insert!(:user, status: :created)
```
