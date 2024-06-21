# Entendendo os Scripts Shell

Scripts shell são programas escritos para o shell do Unix/Linux. Eles permitem automatizar tarefas repetitivas e realizar operações complexas de maneira eficiente. Nesta aula, vamos explorar os conceitos básicos de scripts shell, como escrevê-los e executá-los.

## O que é um Script Shell?

Um script shell é um arquivo texto contendo uma série de comandos que são executados em sequência pelo interpretador de comandos do Unix/Linux. Ele pode ser usado para automatizar tarefas de manutenção, realizar backups, processar arquivos, entre outros.

## Primeiros Passos com Scripts Shell

- Criando e Executando um Script Simples:
  Criar um arquivo de script: Crie um arquivo chamado meu_script.sh.

```
nano meu_script.sh
```

- Adicionar comandos ao arquivo: Adicione o seguinte conteúdo ao arquivo.

```
#!/bin/bash
echo "Olá, mundo!"
```

-- `#!/bin/bash:` Indica que o script deve ser executado pelo interpretador de comandos bash.
-- echo "Olá, mundo!": Imprime "Olá, mundo!" no terminal.
Salvar e sair do editor: No nano, use Ctrl + O para salvar e Ctrl + X para sair.

- Tornar o script executável: Altere as permissões do arquivo para torná-lo executável.

```
chmod +x meu_script.sh
```

Executar o script: Execute o script usando ./.

```
./meu_script.sh
```

## Elementos Básicos dos Scripts Shell

- Comentários
  Os comentários são usados para documentar o código e são ignorados pelo interpretador.

```
# Este é um comentário
echo "Este é um comando"
```

- Variáveis
  As variáveis armazenam dados que podem ser usados e modificados ao longo do script.

```
#!/bin/bash
nome="João"
echo "Olá, $nome!"
```

- Entrada do Usuário
  O comando read permite capturar a entrada do usuário.

```
#!/bin/bash
echo "Digite seu nome:"
read nome
echo "Olá, $nome!"
```

- Condicionais
  Os comandos condicionais permitem executar blocos de código baseados em condições.

```
#!/bin/bash
echo "Digite um número:"
read numero

if [ $numero -gt 10 ]; then
  echo "O número é maior que 10."
else
  echo "O número é 10 ou menor."
fi
```

- Laços de Repetição
  Os laços permitem executar comandos repetidamente.

```
#!/bin/bash
for i in {1..5}
do
  echo "Contagem: $i"
done
```
