# hostsWindowns
Configurar hosts no Windowns usando o Xampp

==========================================

Configurando Host no Windows

*Entrar em C:\xampp\apache\conf e procurar por:
DocumentRoot "C:/www" ==> (esse é o diretório onde encontra o meu projeto)

<Directory "C:/www">    
    Options Indexes FollowSymLinks Includes ExecCGI
    AllowOverride All
    Require all granted
</Directory>

*Entrar em C:\xampp\apache\conf\extra\httpd-vhosts.conf
Criar:

<VirtualHost *:80>
    ServerAdmin desafio.site
    DocumentRoot "C:\www\cesar\assessment-backend-xp\site\public_html" ==> (diretório onde encontra o projeto)
    ServerName desafio.site ==> (nome que vou dar para acessar pela url no navegador)
    ErrorLog "logs/local.projeto.com-error.log"
    CustomLog "logs/local.projeto.com--access.log" common
</VirtualHost>

*Entrar C:\Windows\System32\drivers\etc\hosts abrir o bloco de nota como admin
127.0.0.1 desafio.site ==> (criar o host aqui com o nome que vai ser acessado na porta 80)

Realizar essa configuração para acessar o sistema no navegador.

==========================================
