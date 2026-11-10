# 🛒 Gerenciador de Estoque Simples em Python

Projeto desenvolvido durante o **Bootcamp Generation Brasil**, com o objetivo de praticar conceitos fundamentais de Python por meio da criação de um sistema simples de gerenciamento de estoque.

O programa permite cadastrar, visualizar e remover produtos, mantendo seus respectivos preços sincronizados.

---

## 🚀 Funcionalidades

- 📦 **Visualização de estoque:** exibe todos os produtos e seus respectivos preços.
- ➕ **Cadastro de produtos:** permite adicionar novos produtos e preços.
- ✅ **Confirmação de cadastro:** informa quando um produto é cadastrado com sucesso.
- 🗑️ **Remoção do último item:** permite remover o último produto cadastrado.
- 🔎 **Busca por nome:** localiza um produto específico pelo nome.
- ❌ **Remoção seletiva:** remove o produto escolhido e seu respectivo preço.
- 🛡️ **Validação:** verifica se o estoque está vazio antes de realizar remoções.

---

## 🛠️ Tecnologias e conceitos utilizados

| Tecnologia / Método | Aplicação |
|---|---|
| Python 3.x | Linguagem de programação |
| Listas (`list`) | Armazenamento de produtos e preços |
| `append()` | Cadastro de novos itens |
| `pop()` | Remoção de itens |
| `index()` | Localização de produtos |
| `zip()` | Percorrer listas simultaneamente |
| `len()` | Verificar quantidade de itens |
| `if / else` | Estruturas condicionais |
| `for` | Estruturas de repetição |
| `input()` | Entrada de dados |
| `lower()` | Padronização de texto |

---

## 📋 Estrutura de dados

O projeto utiliza **listas paralelas**, mantendo os produtos e seus preços relacionados pelo mesmo índice.

```python
produtos = [
    "Camiseta Básica",
    "Calça Jeans",
    "Jaqueta Corta-Vento"
]

precos = [49.90, 129.90, 219.90]
```

Exemplo da organização:

| Índice | Produto | Preço |
|---|---|---:|
| 0 | Camiseta Básica | R$ 49,90 |
| 1 | Calça Jeans | R$ 129,90 |
| 2 | Jaqueta Corta-Vento | R$ 219,90 |

---

## 💻 Exemplos de código

### 1. Cadastro de produtos

Utilizando `input()` para receber os dados e `append()` para adicionar novos elementos.

```python
novo_produto = input("Nome do produto: ")
novo_preco = float(input("Preço: R$ "))

produtos.append(novo_produto)
precos.append(novo_preco)

print("Produto cadastrado com sucesso!")
```

### 2. Visualização do estoque

Utilizando `zip()` para percorrer as duas listas simultaneamente.

```python
for produto, preco in zip(produtos, precos):
    print(f"{produto} - R$ {preco:.2f}")
```

### 3. Remoção do último produto

Utilizando `len()` para verificar se existem produtos antes de executar `pop()`.

```python
if len(produtos) > 0:

    produto_removido = produtos.pop()
    preco_removido = precos.pop()

    print("Produto removido:", produto_removido)
    print(f"Preço: R$ {preco_removido:.2f}")

else:
    print("Estoque vazio!")
```

### 4. Busca e remoção por nome

Utilizando `lower()` para facilitar a comparação dos nomes e `index()` para localizar a posição do produto.

```python
item = input("Digite o produto que deseja remover: ").lower()

produtos = [produto.lower() for produto in produtos]

if item in produtos:

    i = produtos.index(item)

    produto_removido = produtos.pop(i)
    preco_removido = precos.pop(i)

    print("Produto removido com sucesso!")
    print("Produto:", produto_removido)
    print(f"Preço: R$ {preco_removido:.2f}")

else:
    print("Produto não encontrado!")
```

---

## 📚 Aprendizados

Durante o desenvolvimento deste projeto, foram praticados:

- Manipulação de listas em Python.
- Entrada e saída de dados.
- Estruturas condicionais e de repetição.
- Busca e remoção de elementos.
- Organização e sincronização de listas.
- Validação de informações.

---

## 🎯 Objetivo do projeto

Consolidar os conhecimentos iniciais em Python por meio de um exercício prático, desenvolvendo a lógica de programação e a capacidade de resolver problemas utilizando estruturas de dados.

---

**Desenvolvido como atividade prática do Bootcamp Generation Brasil.** 🐍
