# Nginx

## História e Introdução

- **Lançamento:** Nginx foi lançado em 2004 por Igor Sysoev.
- **Desenvolvedor:** Inicialmente desenvolvido por Igor Sysoev, agora mantido pela empresa Nginx, Inc. e pela comunidade de código aberto.
- **Popularidade:** Nginx é conhecido por sua alta performance, baixo uso de recursos e escalabilidade, sendo amplamente adotado para servir grandes volumes de tráfego.

## Conceitos Principais

1. Processamento de Requisições

- **Modelo de Processamento:** Nginx usa um modelo baseado em eventos e arquitetura assíncrona. Em vez de criar um novo processo ou thread para cada solicitação, Nginx pode lidar com milhares de conexões simultâneas em um número fixo de processos de trabalho.
- **Eventos:** Cada solicitação é tratada como um evento, e um único thread pode gerenciar muitas conexões simultaneamente.

2. Configuração

- **Arquivos de Configuração:** O principal arquivo de configuração é `nginx.conf.` Também utiliza arquivos de configuração adicionais para servidores virtuais.
- **Blocos de Configuração:** Usa blocos de configuração como http, server, location para organizar a configuração.
- - **http:** Configurações globais para o servidor HTTP.
- - **server:** Configurações específicas para um servidor virtual.
- - **location:** Configurações específicas para determinadas URLs ou diretórios.

3. Módulos

- **Modularidade:** Embora menos modular que o Apache, Nginx inclui muitos módulos essenciais por padrão.
- **Carregamento de Módulos:** Os módulos em Nginx geralmente são compilados no binário principal, e não são carregáveis dinamicamente como no Apache.

4. Segurança

- **SSL/TLS:** Suporte robusto para criptografia com o módulo `ngx_http_ssl_module`.
- **Controle de Acesso:** Configurações de controle de acesso através de diretivas como `allow` e `deny`.

5. Desempenho

- **Caching:** Suporte a caching eficiente através de `proxy_cache`, `fastcgi_cache`.
- **Balanceamento de Carga:** Capacidade de balancear carga entre servidores backend usando várias estratégias de balanceamento.
- **Compressão:** Suporte para compressão de conteúdo com o módulo `ngx_http_gzip_module`.

6. Casos de Uso

- **Servir Conteúdo Estático:** Nginx é extremamente eficiente em servir conteúdo estático, como arquivos HTML, CSS, JavaScript, imagens e vídeos.
- **Proxy Reverso:** Frequentemente usado como um proxy reverso para distribuir a carga entre servidores backend, melhorar a segurança e oferecer caching.
