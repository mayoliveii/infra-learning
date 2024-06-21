# Manipulação de Arquivos e Diretórios no Linux

A manipulação de arquivos e diretórios é uma habilidade fundamental para qualquer usuário de Linux. Neste tópico, aprenderemos como criar, visualizar, mover, copiar e excluir arquivos e diretórios utilizando comandos do terminal. Esta aula é baseada no Capítulo 3 do livro "The Linux Command Line".

## Atividade Prática

- Passo 1: Criação e Navegação
  Crie um diretório chamado projeto.

```
mkdir projeto
```

Entre no diretório projeto.

```
cd projeto
```

- Passo 2: Criação de Arquivos
  Crie um arquivo chamado leia_me.txt.

```
touch leia_me.txt
```

Edite o arquivo leia_me.txt com o nano ou vim e adicione algum texto.

```
nano leia_me.txt
```

ou

```
vim leia_me.txt
```

- Passo 3: Cópia e Movimentação
  Copie o arquivo leia_me.txt para leia_me_copia.txt.
  bash
  Copy code
  cp leia_me.txt leia_me_copia.txt
  Mova o arquivo leia_me_copia.txt para o diretório home do usuário.

```
mv leia_me_copia.txt ~
```

- Passo 4: Visualização e Remoção
  Visualize o conteúdo de leia_me.txt.

```
cat leia_me.txt
```

Remova o arquivo leia_me.txt.

```
rm leia_me.txt
```

## Conclusão

A manipulação de arquivos e diretórios é uma habilidade essencial para trabalhar eficientemente no Linux. Praticar esses comandos básicos ajuda a construir uma base sólida para operações mais avançadas e administração de sistemas.
