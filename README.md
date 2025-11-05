# 🧮 Script SQL - Operadores Aritméticos no MySQL

Este projeto demonstra o uso dos **principais operadores aritméticos** no MySQL, aplicados tanto a cálculos simples quanto a expressões dentro de consultas SQL.

---

## 🎯 Objetivo
Apresentar exemplos práticos do uso de **operações matemáticas** diretamente em comandos SQL, incluindo:
- Soma, subtração, multiplicação e divisão
- Módulo (resto de divisão)
- Expressões combinadas
- Aplicação em consultas com dados reais (exemplo de projeção populacional)

---

## ⚙️ Operadores Demonstrados

| Operador | Função | Exemplo |
|-----------|---------|----------|
| `+` | Soma | `select 1+3 as retorno;` |
| `-` | Subtração | `select 5-2 as retorno;` |
| `*` | Multiplicação | `select 3*2 as retorno;` |
| `/` | Divisão | `select 15/3 as retorno;` |
| `%` | Módulo (resto da divisão) | `select 12%5 as retorno;` |

---

## 🧩 Expressões Combinadas
Exemplo de operação mais complexa utilizando parênteses:

select ((1+4)*(3*3))/5 as retorno;
Esse cálculo primeiro soma, depois multiplica e por fim divide, respeitando a precedência de operadores.

🌎 Aplicações em Consultas
Os exemplos a seguir simulam projeções populacionais com base em uma tabela chamada senso.

🔺 Acréscimo de 10% na população
(sql)
select nome_mun, populacao,
       populacao*1.10 as pop_projecao
from senso
where ano = '2014';
Projeta um aumento de 10% sobre o valor atual da população.

🧮 Cálculo separado de acréscimo e projeção
(sql)
select nome_mun, populacao,
       populacao*0.10 as acrescimo,
       populacao + (populacao*0.10) as projecao_pop
from senso
where ano = '2014';
🔻 Decréscimo de 10% na população
(sql)
select nome_mun, populacao,
       populacao*0.10 as acrescimo,
       populacao - (populacao*0.10) as projecao_pop
from senso
where ano = '2014';
🧠 Exemplo prático com divisão e módulo
Demonstra como o operador % retorna o resto da divisão:

(sql)
select 38/5 as divisao,
       38%5 as restante;
Resultado:

Divisão: 7

Resto: 3

📚 Conceitos Reforçados
Operadores aritméticos básicos e compostos

Precedência de operações em SQL

Uso de expressões matemáticas em SELECT

Projeções e variações de valores em colunas numéricas

