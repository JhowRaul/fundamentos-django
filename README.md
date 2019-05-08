Fundamentos Django 2.0

![Ciclo Request-Response Django](http://i.stack.imgur.com/rLfSC.jpg)

Para git CMD:

```bash
git clone https://github.com/JhowRaul/fundamentos-django.git
git add .

echo --global somente no próprio computador

git config --global user.email "jhowopet@gmail.com"
git config --global user.name "Jhow"

git commit -m "Initial commit"
git push origin master
```

```bash
git add .
git commit -m "<digite seu comentário>"
git push origin master
```

Passo a passo para criação de projeto web Django (apenas comandos):

0) Crie o diretório (pasta) do projeto 
1) Crie o ambiente de desenvolvimento isolado python (virtual env):

Nota: Caso já tenha um virtual env ativo, use este código para desativar
```bash
dactivate
```

```bash
python -m venv venv
cd venv/Scripts
activate
cd ..
cd ..
```

2) Instalar Django na venv:
```bash
pip install django
```

3) Se foi um sucesso, crie a aplicação web (via lib django-admin):
```bash
django-admin startproject nome_da_aplicacao
```

4) Criar API Django (ja vem com SQLite3 configurado, mas pode ser trocado):
```bash
python manage.py startapp nome_da_api
```
Para rodar a aplicação em um servidor local:
```bash
python manage.py runserver
```

A partir daqui é o passo a passo para criação do banco de dados, gerenciamento das migrations e criação de um superuser.

5) Criar o banco:
```bash
python manage.py migrate
```

6) Criação de um superuser (via lib django-admin):
```bash
python manage.py createsuperuser
```

Após realizar as modificações no projeto (criação de class em models.py e registrar a model em admin.py)
7) Criação e modificações nas tabelas (SQL):
```bash
python manage.py makemigrations

# Caso ocorra algum erro use também:
python manage.py migrate--run-syncdb
```

Código desenvolvido durante o curso: https://www.youtube.com/playlist?list=PLHWfNMxB2F4HdKbo8zdgXyxVDOxH429Ko
