# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas linguagens Python, JavaScript, TypeScript e Java, e gera relatórios `HTML` como [este](https://andrehora.github.io/gitevo-examples/python/pandas.html).

Mais exemplos de relatórios podem ser podem ser encontrados em https://github.com/andrehora/gitevo-examples.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

> [!NOTE]
> Antes de instalar a ferramenta, é recomendado criar e ativar um [ambiente virtual Python](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#create-and-use-virtual-environments).

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
$ pip install gitevo
```

Execute a ferramenta no repositório selecionado utilizando o comando abaixo (ajuste conforme a linguagem do repositório).
Substitua `<git_url>` pela URL do repositório que será analisado:

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r javascript <git_url>

# TypeScript
$ gitevo -r typescript <git_url>

# Java
$ gitevo -r java <git_url>
```

Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

> [!NOTE]
> Essa etapa pode demorar alguns minutos pois o projeto será clonado e analisado localmente.

# Passo 3: Explorar o relatório de evolução de código

Após executar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), é gerado um relatório `HTML` contendo diversos gráficos sobre a evolução do código.

Abra o relatório `HTML` e observe com atenção os gráficos.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo
- Detalhar se as curvas estão de acordo com boas práticas
- Explicar grandes alterações nas curvas
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- etc.

Seja criativo!

# Instruções para o exercício

1. Crie um `fork` deste repositório (mais informações sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Adicione o relatório `HTML` no seu fork.
3. No Moodle, submeta apenas a URL do seu `fork`.

Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork:

1. Repositório selecionado: [immich](https://github.com/immich-app/immich)
2. Gráfico selecionado: 

![Gráfico de quantidade de comentários em código](imgs/CommentsGraphs.png)

3. Explicação: 

**Detalhar a evolução ao longo do tempo:** É possível notar que a quantidade de comentários no código apenas aumentaram desde a criação em 2022 até o ápice em 2024 com mais de 5000 comentários. Contudo, a partir desse ponto os comentários caíram ao longo do ano de 2025 até 1000 comentários.

**Detalhar se as curvas estão de acordo com boas práticas:** No começo, o crescimento da quantidade de comentários é um sinal de má prática, pois é uma forma de evitar boas práticas de código limpo e legível.

**Explicar grandes alterações nas curvas:** A partir de 2024, o time de desenvolvimento pode focar totalmente apenas no desenvolvimento de immich e conseguiram expandi-lo. Nesse ponto, os desenvolvedores decidiram fazer reestruturações na arquitetura do projeto e aplicar boas práticas, aproveitando essa oportunidade de refatorar o sistema.

**Explorar a documentação do repositório em busca de explicações para grandes alterações:** Um exemplo dessas mudanças foi que, em 2025, o time de desenvolvimento fez grandes mudanças em vários componentes, re-escrevendo diversos componentes desde suas bases, o que levou a eliminar muito código legado com vários comentários.

Um exemplo de uma das falas do time de desenvolvimento sobre essa grande reestruturação foi feito neste post do reddit: [Dear developers, please stabilize the basics before adding new features](https://www.reddit.com/r/immich/comments/1mx3eu0/dear_developers_please_stabilize_the_basics/).
