# Modelo dissertação PPGCC

Modelo de dissertação baseado no template da [ABNTex2](https://github.com/abntex/abntex2) (Trabalho acadêmico). Esse projeto
tem como finalidade facilitar a escrita da dissertação dos mestrandos do [Programa de Pós-Graduação em Ciência da Computação (PPGCC)](http://ppgcc.ifce.edu.br) do Instituto Federal do Ceará (IFCE).

## Por onde começar?

1. Faça um clone do projeto `git clone https://github.com/omadson/modelo-dissertacao-ppgcc minha-dissertacao` ou baixe o [.ZIP](https://github.com/omadson/modelo-dissertacao-ppgcc/archive/master.zip)
2. Modifique o arquivo `informacoes.tex` com suas próprias informações
3. _Hands-on_

## Funcionalidades
O projeto conta com algumas facilidades:
 - Arquivo contendo todas as informações em separado, dessa maneira você não se repete
 (DRY - don't repeat yourself).
 - Diretórios específicos para capítulos, anexos, apêndices e figuras. Dessa
 maneira você tem um projeto mais organizado.

## Utilizando o projeto
Para melhor utilização do projeto, você deve seguir algumas boas práticas.

O arquivo `informacoes.tex` contém os dados relacionados ao seu trabalho, tais como, título,
autor, área de concentração, orientador etc. Caso você não tenha um coorientador, basta
apagar a linha referente.

Cada capítulo deve ser salvo separadamente no diretório `capitulos`. Como no exemplo abaixo:

```
modelo-dissertacao-ppgcc
├── capitulos
│   ├── conclusao.tex
│   ├── capitulo-exemplo.tex
│   ├── ...
│   └── introducao.tex
├── dissertacao.tex
├── informacoes.tex
...
├── README.md
└── referencias.bib
```
Imagens e gráficos devem ser colocados no diretório `figuras/imagens` e
`figuras/graficos` respectivamente.

Elementos pré-textuais devem residir no diretório `pretextual`, tais como o `resumo.tex`,
`abstract.tex`, `dedicatoria.tex`, entre outros já listados lá.

Os diretórios `apendices` e `anexos` guardam os apêndices e anexos respectivamente.

As tabelas devem ser salvas no diretório `tabelas` e para adicionar uma tabela, basta inserir o comando `\includetable{<nome-da-tabela>}` dentro do arquivo que você está editando.

O arquivo que deve ser compilado é o `dissertacao.tex`, após a compilação, você deve ter
disponível no seu diretório de trabalho o arquivo `dissertacao.pdf`.

## Facilitadores
Facilitadores são comandos que facilitam o uso de outros comandos. Como por exemplo, a inclusão
de imagens. Dois comandos foram criados para simplificar essa inclusão. Os comandos são
`\figurasimples` e `\figuradupla`.

O comando `\figurasimples` recebe 3 parâmetros. 

```
% sintaxe:
\figurasimples{nome-do-arquivo}{Legenda da imagem}{tamanho}

% exemplo:
\figurasimples{logo-ifce-sem-nome}{Logotipo do IFCE sem nome}{4cm}
```

O comando `\figuradupla` recebe 4 parâmetros.
```
% sintaxe:
\figuradupla{nome-do-arquivo-1}{Legenda da imagem 1}
{nome-do-arquivo-2}{Legenda da imagem 2}

% exemplo:
\figuradupla{logo-ifce-sem-nome}{Logotipo do IFCE sem nome}
{logo-ifce-padrao}{Logotipo do IFCE padrão}
```

## Dúvidas?
 - [Madson Dias](http://github.com/omadson)
 - [Vitor Carvalho](http://github.com/vitorcarvalhoml)

## Veja também
 - [Modelo de apresentação PPGCC](https://github.com/vitorcarvalhoml/modelo-apresentacao-ppgcc)