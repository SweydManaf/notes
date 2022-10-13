# Testes

## Para quê testes?

A ideia principal dos testes é garantir que eles funcionem de fato. Então para desenvolver um bom software ele precisa funcionar como esperado. E dependendo de como os testes são executados, mais rápido vai ter um feedback de que ele está como deveria.

## Quando escrever testes?

SEMPRE. O bom de escrever testes é que diferentes tarefas manuais completamente chatas. Eles vão durar sempre.

## xUnit-Style

xUnit é uma filosofia de Framework de testes. Ele nasceu no Smalltalk e lá se chamava SUnit.

- Test case class
    - Classe base para todas as classes de testes.
- Test fixtures
    - Funções ou métodos que são executados antes e depois da execução dos blocos do código de teste.
- Assertions
    - Funções ou métodos são usados para verificar o comportamento do componente que está sendo testado.
- Test runner
    - Programa ou bloco de código que executa o conjunto de testes.