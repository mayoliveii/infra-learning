# Introdução ao Linux e Navegação no Sistema de Arquivos

## Introdução ao Linux

Linux é um sistema operacional de código aberto amplamente utilizado tanto em servidores quanto em desktops. Ele é conhecido por sua robustez, segurança e flexibilidade. O núcleo do Linux (kernel) foi desenvolvido por Linus Torvalds em 1991, e desde então, várias distribuições (distros) foram criadas, como Ubuntu, Fedora, Debian, entre outras.

1. Componentes do Linux

- **Kernel:** O núcleo do sistema operacional que gerencia recursos de hardware e software.
- **Shell:** Interface que permite ao usuário interagir com o kernel.
- **Sistema de Arquivos:** Estrutura que organiza e armazena dados no disco.

2. Distribuições Linux
   As distribuições Linux são versões do sistema operacional que combinam o kernel com pacotes de software adicionais. Cada distro pode ter um foco específico, como facilidade de uso (Ubuntu), estabilidade (Debian) ou inovação (Fedora).

## Instalação de uma Distribuição Linux

Para a atividade prática, vamos instalar o Ubuntu em uma máquina virtual usando o VirtualBox. Aqui estão os passos detalhados:

1. Baixar e Instalar o VirtualBox

- Acesse o site do VirtualBox.
- Baixe a versão adequada para o seu sistema operacional (Windows, macOS, Linux).
- Siga as instruções de instalação.

2. Baixar o Ubuntu

- Vá para o site do Ubuntu.
- Baixe a imagem ISO da versão mais recente do Ubuntu.

3. Criar uma Máquina Virtual

- Abra o VirtualBox e clique em "New" para criar uma nova máquina virtual.
- Dê um nome à máquina (por exemplo, "Ubuntu VM") e selecione "Linux" como tipo e "Ubuntu" como versão.
- Configure a memória RAM (recomenda-se pelo menos 2 GB).
- Crie um disco rígido virtual (recomenda-se 20 GB ou mais).
- Siga as instruções para finalizar a criação da máquina.

4. Instalar o Ubuntu na Máquina Virtual

- Selecione a máquina virtual criada e clique em "Start".
- Escolha o arquivo ISO do Ubuntu baixado anteriormente.
- Siga as instruções na tela para instalar o Ubuntu. Isso inclui selecionar o idioma, configurar o teclado, definir partições (opte por "Instalar Ubuntu ao lado do sistema operacional existente" ou "Apagar disco e reinstalar Ubuntu" se estiver em um VM), e criar um usuário.

3. Navegação no Sistema de Arquivos

- Uma vez instalado o Ubuntu, podemos iniciar a navegação pelo sistema de arquivos utilizando comandos básicos de terminal.
- Abertura do Terminal: Para abrir o terminal, você pode usar o atalho Ctrl + Alt + T ou procurar por "Terminal" no menu de aplicativos.

### Comandos Básicos de Navegação

- pwd (Print Working Directory):
  Exibe o diretório atual em que você está.

```
pwd
```

- ls (List):
  Lista os arquivos e diretórios no diretório atual.

```
ls
```

Usando opções:

```
ls -l    # lista detalhada
ls -a    # inclui arquivos ocultos
ls -la   # lista detalhada incluindo arquivos ocultos
```

- cd (Change Directory):
  Muda o diretório atual.

```
cd /caminho/para/diretorio
```

- man (Manual):
  Mostra o manual de um comando.

```
man ls
```

- touch:
  Cria um arquivo vazio ou atualiza a data de modificação de um arquivo existente.

```
touch arquivo.txt
```

- mkdir (Make Directory):
  Cria um novo diretório.

```
mkdir novo_diretorio
```

- rm (Remove):
  Remove arquivos ou diretórios.

```
rm arquivo.txt           # remove um arquivo
rm -r diretorio          # remove um diretório e seu conteúdo
```

Opções comuns:

-r: Remove diretórios recursivamente
-f: Força a remoção sem perguntar

- cp (Copy):
  Copia arquivos ou diretórios.

```
cp origem destino
cp -r diretorio_origem diretorio_destino
```

- mv (Move):
  Move ou renomeia arquivos ou diretórios.

```
mv arquivo_origem novo_local
mv nome_antigo novo_nome
```

**Editores de Texto (nano e vim)**
Para editar arquivos de texto, você pode usar editores de texto no terminal como nano ou vim.

- nano:

```
nano arquivo.txt
```

Navegação básica: Use as setas do teclado.
Salvar: `Ctrl + O`, seguido de Enter.
Sair: `Ctrl + X`.

- vim:

```
vim arquivo.txt
```

Modo de inserção: Pressione `i` para entrar no modo de inserção.
Salvar e sair: Pressione Esc, digite `:wq` e pressione Enter.
Sair sem salvar: Pressione Esc, digite `:q!` e pressione Enter.

- rmdir (Remove Directory)
  Remove diretórios vazios.

```
rmdir nome_do_diretorio
```

- cat (Concatenate)
  Exibe o conteúdo de arquivos.

```
cat arquivo.txt
```

- less
  Exibe o conteúdo de arquivos de forma paginada.

```
less arquivo.txt
```

- head
  Exibe as primeiras linhas de um arquivo.

```
head -n 10 arquivo.txt
```

- tail
  Exibe as últimas linhas de um arquivo.

```
tail -n 10 arquivo.txt  # Exibe as últimas 10 linhas
```

- sort
  Ordena as linhas de um arquivo.

```
sort arquivo.txt
```

Opções:
-r: Ordem reversa
-n: Ordem numérica

- uniq
  Remove linhas duplicadas consecutivas em um arquivo. Normalmente usado em combinação com sort.

```
sort arquivo.txt | uniq
```

Opções:
-c: Conta as ocorrências de cada linha única

## Conclusão

Linux é um sistema operacional poderoso e flexível, ideal para desenvolvimento de software e administração de sistemas. A navegação pelo sistema de arquivos é fundamental para trabalhar de forma eficiente no Linux. Praticar esses comandos básicos ajudará a construir uma base sólida para explorar comandos mais avançados e administrar o sistema de forma eficaz.
