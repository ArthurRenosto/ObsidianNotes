
## 🧱 Classe

A **classe** é o **molde / projeto / blueprint**.

Ela define:

✅ quais dados o objeto terá (atributos)  
✅ quais ações ele pode fazer (métodos)

Exemplo mental:

> Classe = planta da casa  
> Casa real = objeto

Em código (Python):

```python
class Pessoa:
    nome = ""
    idade = 0
```

Aqui você só definiu o **modelo**. Nada existe ainda.

---

## ⚙️ Método

O **método** é uma **função dentro da classe**.

Ele define o comportamento do objeto.

```python
class Pessoa:
    def falar(self):
        print("Oi!")
```

`falar()` é um método.

👉 Método = ação  
👉 Função normal = fora da classe  
👉 Método = dentro da classe

---

## 🧍 Instância (objeto)

A **instância** é quando você cria algo real a partir da classe.

```python
p1 = Pessoa()
```

Agora:

- `Pessoa` → classe
    
- `p1` → instância (objeto)
    

Ou seja:

> Você “materializou” o molde.

---

## Exemplo completo

```python
class Pessoa:
    def __init__(self, nome):
        self.nome = nome

    def falar(self):
        print(f"Meu nome é {self.nome}")

p1 = Pessoa("Arthur")   # instância
p1.falar()             # chama método
```

### O que está acontecendo:

### 1️⃣ Classe

```python
class Pessoa:
```

Define o modelo.

---

### 2️⃣ Método

```python
def falar(self):
```

Função da classe.

---

### 3️⃣ Instância

```python
p1 = Pessoa("Arthur")
```

Objeto real criado.

---

## Resumo rápido (pra gravar):

### 🔹 Classe

Molde / estrutura

### 🔹 Método

Função da classe

### 🔹 Instância

Objeto criado a partir da classe

---

Se quiser, posso explicar também:

✅ `self`  
✅ `__init__`  
✅ atributos  
✅ exemplo em C  
✅ exemplo em C++  
✅ exemplo mais hacker-oriented (tipo modelar um Host/Service/Exploit 😈)

Só dizer.