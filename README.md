# formularios

Guia de Configuração do Formulário no Servidor Este guia detalha as etapas necessárias para configurar o ambiente do servidor, garantindo o funcionamento correto do formulário gerado. Siga os passos abaixo para instalar e configurar todas as dependências exigidas.

Servidor Web Dependência: Apache ou Nginx O servidor web será responsável por hospedar o site.
Atualize os pacotes do sistema:

sudo apt update

Instale o Apache: sudo apt install apache2

PHP
Dependência: PHP com extensões necessárias O PHP será utilizado para processar o formulário e enviar os e-mails.

Instalação do PHP e extensões:

sudo apt install php php-cli php-mbstring php-xml php-curl php-common php-mysql

Configuração de E-mail (SMTP com Gmail) Dependência: Configuração do envio de e-mails utilizando Gmail O formulário utiliza a função mail() do PHP em conjunto com o protocolo SMTP do Gmail.
Etapas para configurar o SMTP do Gmail:

sudo apt install msmtp-mta

Permissões e Propriedades Ajuste as permissões do diretório onde o formulário será hospedado para que o servidor tenha acesso adequado.
sudo chown -R www-data:www-data /var/www/html/formulario

sudo chmod -R 755 /var/www/html/formulario

PHPMailer (Alternativa Recomendável) Para um envio de e-mails mais confiável, recomenda-se o uso da biblioteca PHPMailer.
Instalação e configuração do PHPMailer:

sudo apt install composer composer require phpmailer/phpmailer
