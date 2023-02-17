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

def build(:user) do
    %User{
      remove_register: false,
      name: PtBr.name(),
      email: "user#{System.unique_integer([:positive])}@payfy.com.br",
      password_hash: Argon2.hash_pwd_salt("A12345a!"),
      cellphone: "+5500999999999",
      cpf: gen_cpf(),
      birth_day: Date.from_iso8601!("1990-01-01"),
      number: System.unique_integer([:positive]),
      street: "some address",
      street_number: "47",
      complement: "some complement",
      postal_code: "3216547",
      state: "SC",
      city: "Florianopolis",
      neighborhood: "Centro",
      status: :activated
    }
  end

```

```
apps/adapters/test/adapters/swap/account_processor_test.exs

user = PayfyFactory.insert!(:user, status: :activated)
...

user = PayfyFactory.insert!(:user, status: :created)
```
