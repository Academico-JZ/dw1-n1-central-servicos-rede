# Central de Serviços de Rede

Projeto desenvolvido para a Avaliação Prática N1 da disciplina Desenvolvimento Web I.

## Identificação

- **Estudante:** Jairuzalon Maguidiel Vieira
- **Matrícula:** 2023015830
- **Curso:** Tecnologia em Redes de Computadores
- **Instituição:** Instituto Federal Catarinense (IFC) — Campus Araquari
- **Disciplina:** RCC0218 — Desenvolvimento Web I

## Objetivo

Aplicação web estática voltada ao ambiente de infraestrutura de redes para apresentação de catálogo de serviços de TI, visualização de chamados técnicos e interface de abertura de novas solicitações de suporte.

## Tecnologias Empregadas

- **HTML5 Semântico:** Estruturação lógica com `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<fieldset>`, `<legend>` e `<footer>`;
- **CSS3 Puro:** Sem dependências ou frameworks externos;
- **Layout com Flexbox:** Distribuição flexível e alinhamento de componentes;
- **Design Responsivo:** Media queries para adaptação em dispositivos móveis e desktops;
- **Constraint Validation API (HTML5):** Validações nativas com `required`, `pattern`, `minlength`, `maxlength` e tipos especializados de `input`.

*Obs.: Não foram utilizados scripts JavaScript ou rotinas de backend, respeitando as diretrizes da avaliação N1.*

## Páginas Desenvolvidas

| Página | Arquivo | Descrição |
| :--- | :--- | :--- |
| **Início** | [`index.html`](index.html) | Página institucional da central com apresentação e grade de cartões de serviços. |
| **Chamados** | [`chamados.html`](chamados.html) | Painel com métricas de chamados, filtros detalhados e listagem das solicitações cadastradas. |
| **Abrir Chamado** | [`abrir-chamado.html`](abrir-chamado.html) | Formulário estruturado em seções lógicas para submissão de chamados técnicos. |

## Estrutura do Repositório

```text
dw1-n1-central-servicos-rede/
├── index.html
├── chamados.html
├── abrir-chamado.html
├── README.md
└── assets/
    ├── css/
    │   ├── reset.css
    │   ├── global.css
    │   ├── index.css
    │   ├── chamados.css
    │   └── abrir-chamado.css
    └── img/
        ├── cloud.svg
        ├── network-support.svg
        ├── security.svg
        └── wifi.svg
```

## Recursos e Funcionalidades

- **Navegação Consistente:** Menu principal compartilhado com indicação de página ativa via `aria-current="page"`;
- **Catálogo de Serviços:** Cards com imagens vetoriais SVG, categorização semântica e textos alternativos;
- **Painel de Métricas:** Contadores visuais para status de chamados (abertos, pendentes e concluídos);
- **Formulário de Busca e Filtros:** Pesquisa por palavra-chave, categoria, prioridade, status, intervalo de datas e horário;
- **Listagem de Chamados:** Cards informando identificador, categoria, solicitante, prioridade, data/hora formatada com tag `<time>` e status visual correspondente;
- **Formulário Completo de Abertura:**
  - Agrupamento semântico por etapas (`fieldset` e `legend`);
  - Tipos variados de entrada (`text`, `email`, `tel`, `date`, `time`, `select`, `radio`, `checkbox`, `file`, `textarea`);
  - Validação estrita de formatos (máscara de telefone via `pattern`, restrições de extensão em upload com `accept`, intervalos de comprimento);
- **Acessibilidade:** Textos alternativos, rótulos explícitos com `<label for>`, foco visível demarcado e suporte a leitores de tela.

## Execução Local

Para visualizar o projeto localmente:
1. Clone ou baixe este repositório;
2. Abra o arquivo `index.html` em qualquer navegador web (Firefox, Chrome, Edge) ou inicie um servidor local simples (ex.: extensão Live Server no VS Code).

## Publicação

- **Repositório:** [https://github.com/Academico-JZ/dw1-n1-central-servicos-rede](https://github.com/Academico-JZ/dw1-n1-central-servicos-rede)
- **GitHub Pages:** [https://academico-jz.github.io/dw1-n1-central-servicos-rede/](https://academico-jz.github.io/dw1-n1-central-servicos-rede/)

## Dificuldades Encontradas e Conclusão

- **Estado de Conclusão:** 100% dos requisitos da avaliação N1 foram atendidos (3 páginas interligadas, destaque visual da página ativa, catálogo com 4 serviços em Flexbox, 6 chamados com indicadores e filtros de busca, formulário de abertura com validações nativas e layout responsivo sem rolagem horizontal no mobile).
- **Dificuldades Encontradas:** O maior desafio consistiu na organização responsiva dos campos do formulário de abertura e dos filtros da listagem de chamados, assegurando que o alinhamento com Flexbox e as restrições de `fieldset`/`legend` se adaptassem confortavelmente a telas de smartphones sem causar quebras visuais ou overflow horizontal. Isso foi sanado utilizando `min-width: 0`, bases flexíveis relativas e regras específicas via media queries.

## Considerações Finais

O projeto atende integralmente ao escopo de front-end estático avaliado na N1. Como evolução futura na disciplina (módulos posteriores com JavaScript), planeja-se implementar a reatividade dinâmica dos filtros, consumo de API assíncrona e persistência em banco de dados.
