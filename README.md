# Exerc-cio-Listas-Generation

Gerenciador de Estoque Simples em Python
Este é um projeto em Python para o gerenciamento básico de um estoque de produtos e seus respectivos preços. O sistema foi desenvolvido como uma solução prática utilizando estruturas de dados lineares (listas paralelas), loops e condicionais para controle de inventário.

🚀 Funcionalidades
Visualização de Estoque: Exibe de forma limpa e formatada todos os produtos cadastrados e seus respectivos preços no formato de moeda local (R$).
Cadastro de Novos Produtos: Permite a adição dinâmica de novos itens informando o nome e o preço através de interações pelo terminal.
Remoção de Itens por Confirmação: Pergunta ao usuário se ele deseja remover o último item cadastrado após a atualização do estoque.
Remoção Direta do Último Item: Protege o sistema verificando se o estoque possui itens cadastrados antes de realizar uma remoção direta.
Remoção Seletiva por Nome: Permite buscar e remover um produto específico informando seu nome exato. Caso não exista, o sistema exibe um aviso amigável.
🛠️ Tecnologias Utilizadas
Python 3.x
Métodos de manipuladores de listas (append(), pop(), index())
Função nativa zip() para iteração paralela de dados
Validação de entrada com tratamento de string (lower())
📁 Estrutura de Dados Utilizada
O projeto utiliza Listas Paralelas para armazenar as informações relacionadas:

produtos: Uma lista contendo as strings com os nomes dos itens.
precos: Uma lista contendo os valores numéricos flutuantes (float) dos produtos.
Ambas são sincronizadas através de seus índices.
