# Apache HTTP Server

## História e Introdução

- **Lançamento:** Apache foi lançado em 1995.
- **Desenvolvedor:** Apache Software Foundation.
- **Popularidade:** É um dos servidores web mais utilizados no mundo. Em vários momentos, foi o servidor mais usado na internet.
- **Arquitetura:** Baseada em módulos. Isso significa que a funcionalidade pode ser estendida através de módulos que podem ser carregados no servidor conforme necessário.

## Conceitos Principais

1. Processamento de Requisições

- **Modelo de Processamento:** Apache usa um modelo de processo baseado em threads (por exemplo, MPM-prefork, MPM-worker, MPM-event). Cada solicitação HTTP é tratada por um processo ou thread separado. Isso pode ser configurado para otimizar o desempenho baseado no tipo de carga de trabalho.
- **MPM (Multi-Processing Module):** O Apache oferece diferentes MPMs que definem como as solicitações são tratadas.
- - **prefork:** Cada processo lida com uma única solicitação. Simples e compatível, mas não escalável para grandes volumes de tráfego.
- - **worker:** Usa threads dentro de processos para lidar com múltiplas solicitações simultaneamente. Melhor desempenho e uso de recursos.
- - **event:** Similar ao worker, mas otimizado para conexões keep-alive.

2. Flexibilidade e Configuração

- **Arquivos de Configuração:** O principal arquivo de configuração é o `httpd.conf`. Pode incluir outros arquivos com diretivas específicas.
- **Diretivas:** São comandos de configuração usados em arquivos de configuração para definir o comportamento do servidor. Exemplos incluem DocumentRoot, ServerName, ErrorLog, entre outros.

3. Módulos

- **Modularidade:** Apache é altamente modular. Existem módulos para autenticação, autorização, cache, reescrita de URL, compressão de conteúdo, etc.
- **Carregamento de Módulos:** Módulos podem ser carregados e descarregados dinamicamente, o que permite uma grande flexibilidade na configuração do servidor.

4. Segurança

- **SSL/TLS:** Suporte robusto para criptografia através do módulo mod_ssl.
- **Controle de Acesso:** Configuração granular de acesso com diretivas como Allow, Deny, Require, e módulos de autenticação como `mod_auth_basic` e `mod_auth_digest`.

5. Desempenho

- **Caching:** Vários módulos de cache disponíveis (`mod_cache`, `mod_file_cache`) para melhorar o desempenho.
- **Balanceamento de Carga:** Módulos como `mod_proxy_balancer` permitem a distribuição de carga entre vários servidores backend.

## Casos de Uso

- **Aplicações Dinâmicas:** Apache é frequentemente usado para servir aplicações dinâmicas onde a flexibilidade e compatibilidade com várias tecnologias são essenciais.
- **Hospedagem Compartilhada:** Sua capacidade de isolar configurações e permissões por diretório é útil para ambientes de hospedagem compartilhada.
