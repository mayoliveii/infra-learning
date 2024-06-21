# Exemplo Prático: Configuração de um Site Simples

Vamos configurar um site simples usando Apache.

1. Crie um Diretório para o Site

```
sudo mkdir -p /var/www/meusite
sudo chown -R $USER:$USER /var/www/meusite
```

2. Crie um Arquivo de Configuração para o Site

Crie um arquivo chamado meusite.conf em `/etc/apache2/sites-available/`.

```
sudo nano /etc/apache2/sites-available/meusite.conf
```

Adicione o seguinte conteúdo:

```
<VirtualHost *:80>
    ServerAdmin webmaster@meusite.com
    ServerName meusite.com
    ServerAlias www.meusite.com
    DocumentRoot /var/www/meusite
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

3. Habilite o Site e Reinicie o Apache

```
sudo a2ensite meusite.conf
sudo systemctl reload apache2
```

4. Crie uma Página HTML Simples

```
echo '<!DOCTYPE html><html><head><title>Meu Site</title></head><body><h1>Olá, Mundo!</h1></body></html>' > /var/www/meusite/index.html
```

5. Acesse o Site

Abra um navegador e digite http://meusite.com (você pode editar o arquivo hosts do seu computador para mapear meusite.com para o endereço IP do seu servidor se estiver testando localmente).
