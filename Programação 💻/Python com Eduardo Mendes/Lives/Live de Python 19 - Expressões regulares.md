Live de Python 19 - Expressões regulares

# Expressões regulares

## O que são expressões regulares?

É um método formal de especificar um padrão de texto ou notação para representar padrões em strings, é composto por símbolos, caracteres e funções especiais, que agrupados com caracteres formam uma expressão.

[Regex Pal](https://www.regexpal.com "Testes de regex")

## Caracteres 

|     |     |
| --- | --- |
| **Meta** | **Faz o que?** |
| .   | Qualquer caractere |
| \[ \] | Lista de caracteres |
| ?   | Anterior pode existir ou não |
| .*  | Qualquer coisa |
| { x } | Anterior aparece x vezes |
| $   | Fim da linha |
| +   | Anterior ao menos uma vez |
| (xy) | Cria grupos |
| ^   | Começo da linha |
| \   | escapa o meta |
| \|  | OU  |
| \[ ^ \] | Lista negada |

## Listas

|     |     |
| --- | --- |
| **Meta** | **Faz o que?** |
| \[0-9\] \| \\d | acha todos os números |
| \[a-z\] \| \\w | acha todas as letras minúsculas |
| \[^0-9\] \| \\D | acha tudo que não seja número |
| \[^a-z\] \| \\W | acha tudo que não sejam letras |

## Exemplos

|     |     |
| --- | --- |
| **Padrão** | **Faz o que?** |
| 9?\[0-9\]{4}-\[0-9\]{4} | Número de telefone ex: 8923-9381 |
| \[M\|m\]\[i\|u\|ü\]ll?er | Miler, muler, müller, Muler, ... |
| (SO\|so\|So\|Os\|OS\|os) | Bucaria variações para SO ou OS |

## Objetos

- Compile
    - Compila uma expressão e a aplica a várias strings
- Search
    - Procura uma expressão em qualquer posição de uma string
- Match\[0\] / Fullmatch\[1\]
    - Procura uma expressão no início de uma string (startwith)
    - Procura uma expressão exatamente igual
- Split
    - Dada uma expressão, fatia os dados
- Findall
    - Retorna uma lista com todos os matchs encontrados
- Finditer
    - Retorna um gerador com todos os matchs, cada um sendo um novo objeto de match.