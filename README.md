# Sistema de Cadastro e Login em Python

1. Este projeto apresenta um sistema simples de **cadastro e login**, utilizando dicionários para armazenar usuários, validação de credenciais e estrutura de repetição. O objetivo é treinar **condições**, **loops**, **dicionários** e **entrada de dados**.

---

## Objetivo

* Verificar se o usuário já existe no sistema
* Validar a senha de usuários cadastrados
* Cadastrar novos usuários automaticamente
* Exibir mensagens personalizadas para cada situação
* Encerrar o processo após login ou cadastro bem-sucedido

---

## Funcionamento do Código

### **1 – Banco de usuários**

O programa inicia com um dicionário contendo usuários já cadastrados:

```python
banco = {
    "A": "123",
    "B": "456",
    "C": "789"
}
```

* Cada chave representa um **usuário**
* Cada valor representa sua **senha**

---

### **2 – Entrada de usuário e senha**

O sistema solicita o nome e a senha digitados:

```python
usuario = input("Digite seu nome de usuário: ").strip()
senha = input("Digite sua senha: ").strip()
```

* `.strip()` remove espaços extras digitados pelo usuário.

---

### **3 – Verificação de login**

Caso o usuário exista no banco:

```python
if usuario in banco:
    if banco[usuario] == senha:
        print(f"Bem-vindo de volta, {usuario}!")
        break
    else:
        print("Senha incorreta. Tente novamente.")
```

* Se a senha estiver correta → login aprovado
* Se a senha estiver errada → sistema repete até acertar

---

### **4 – Cadastro automático**

Se o usuário **não existir**, ele é automaticamente registrado:

```python
else:
    banco[usuario] = senha
    print(f"Usuário '{usuario}' cadastrado com sucesso!")
    print(f"Bem-vindo, {usuario}!")
    break
```

* O novo usuário é adicionado ao dicionário
* O sistema encerra após cadastrar e dar boas-vindas

---

## Exemplo de Execução

```
=== Sistema de Cadastro e Login ===
Digite seu nome de usuário: A
Digite sua senha: 123
Bem-vindo de volta, A!
```

Ou:

```
=== Sistema de Cadastro e Login ===
Digite seu nome de usuário: Murilo
Digite sua senha: 999
Usuário 'Murilo' cadastrado com sucesso!
Bem-vindo, Murilo!
```
---
