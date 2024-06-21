# Introdução aos Servidores Web

Um servidor web é um software que serve páginas web para os usuários. Os servidores web mais comuns são o Apache HTTP Server e o Nginx. Eles aceitam solicitações HTTP dos clientes (geralmente navegadores web) e respondem com arquivos HTML, CSS, JavaScript, imagens, etc.

## Passos Básicos para Configurar um Servidor Web

### Preparação do Ambiente

- Escolha do Sistema Operacional: A maioria dos servidores web roda em sistemas Linux (como Ubuntu, Debian, CentOS).
- Acesso ao Servidor: Você precisa de acesso root ou de um usuário com privilégios sudo.

**Instalação do Servidor Web**

- Instalação do Apache no Ubuntu

```
sudo apt update
sudo apt install apache2
```

- Instalação do Nginx no Ubuntu

```
sudo apt update
sudo apt install nginx
```

**Configuração Básica**

- Apache

-Arquivos de Configuração: Os principais arquivos de configuração estão em `/etc/apache2`.

-Diretivas de Configuração: Você pode editar o arquivo `/etc/apache2/apache2.conf` ou adicionar novos arquivos de configuração em `/etc/apache2/sites-available/`.

-Habilitar um Site: Crie um arquivo de configuração para seu site em `/etc/apache2/sites-available/` e habilite-o com:

```
sudo a2ensite nome_do_seu_site.conf
sudo systemctl reload apache2
```

- Nginx

-Arquivos de Configuração: Os principais arquivos de configuração estão em `/etc/nginx`.

-Diretivas de Configuração: Você pode editar o arquivo `/etc/nginx/nginx.conf` ou adicionar novos arquivos de configuração em `/etc/nginx/sites-available/`.

-Habilitar um Site: Crie um arquivo de configuração para seu site em `/etc/nginx/sites-available/` e habilite-o com:

```
sudo ln -s /etc/nginx/sites-available/nome_do_seu_site /etc/nginx/sites-enabled/
sudo systemctl reload nginx
```

**Testar a Configuração**

Após configurar o servidor, é importante testar para garantir que tudo está funcionando corretamente.

- Apache: Verifique a sintaxe da configuração e reinicie o serviço.

```
sudo apache2ctl configtest
sudo systemctl restart apache2
```

- Nginx: Verifique a sintaxe da configuração e reinicie o serviço.

```
sudo nginx -t
sudo systemctl restart nginx
```

**Gerenciamento do Servidor Web**

- Logs: Monitore os logs para identificar problemas.

-Apache: `/var/log/apache2/`

-Nginx: `/var/log/nginx/`

- Segurança: Implemente boas práticas de segurança, como:
- - Usar firewalls (UFW, iptables).
  - Configurar HTTPS com certificados SSL/TLS.
  - Manter o servidor atualizado com patches de segurança.
