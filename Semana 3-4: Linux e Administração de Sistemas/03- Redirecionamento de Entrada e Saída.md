# Redirecionamento de Entrada e Saída

Este é um conceito fundamental que permite manipular a maneira como os comandos do terminal recebem e enviam dados.

## Redirecionamento de Saída

- `>` (Redirecionamento de Saída)
  O símbolo `>` redireciona a saída padrão (stdout) de um comando para um arquivo. Se o arquivo já existir, ele será sobrescrito.

```
comando > arquivo.txt
```

Exemplo:

```
echo "Olá, mundo!" > mensagem.txt
```

Neste exemplo, o texto "Olá, mundo!" é salvo no arquivo mensagem.txt. Se mensagem.txt já existia, ele será substituído.

> obs: Quando você vê `dquote>` no terminal, significa que você abriu uma aspas dupla (") e não a fechou. O shell está esperando que você termine a string que começou. Para resolver isso, você pode fechar a string: `"  # Adicione a aspas dupla final aqui e pressione Enter`

- `>>` (Anexar Redirecionamento de Saída)
  O símbolo `>>` redireciona a saída padrão de um comando para um arquivo, mas em vez de sobrescrever, ele anexa ao final do arquivo.

```
comando >> arquivo.txt
```

Exemplo:

```
echo "Mais uma linha" >> mensagem.txt
```

Neste exemplo, "Mais uma linha" será adicionado ao final de mensagem.txt sem apagar o conteúdo existente.

## Redirecionamento de Entrada

- `<` (Redirecionamento de Entrada)
  O símbolo `<` redireciona a entrada padrão (stdin) de um comando a partir de um arquivo.

```
comando < arquivo.txt
```

Exemplo:

```
cat < mensagem.txt
```

Neste exemplo, o comando cat lê a entrada do arquivo mensagem.txt em vez do teclado.

- Pipes: `|` (Pipe)
  O símbolo `|` redireciona a saída padrão de um comando como entrada padrão para outro comando. Isso permite combinar comandos de maneira poderosa.

```
comando1 | comando2
```

Exemplo:

```
cat arquivo.txt | sort | uniq
```

Neste exemplo:
-cat arquivo.txt exibe o conteúdo de arquivo.txt.
-sort ordena o conteúdo.
-uniq remove as linhas duplicadas consecutivas.

## Resumo

- `>` redireciona a saída de um comando para um arquivo, sobrescrevendo-o.
- `>>` redireciona a saída de um comando para um arquivo, anexando ao final.
- `<` redireciona a entrada de um comando a partir de um arquivo.
- `|` redireciona a saída de um comando como entrada para outro comando.
  Esses operadores são ferramentas poderosas para manipulação de dados no terminal, permitindo criar pipelines de processamento de dados complexos com comandos simples. Praticar esses conceitos ajudará a dominar a utilização do terminal no Linux.
