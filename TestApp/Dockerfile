#de onde eu to tirando a imagem 
FROM tiangolo/uwsgi-nginx-flask:python3.6-alpine3.7

#Oque eu quero que rode, nesse caso instalar o bash e o editor nano 
RUN apk --update add bash nano

#ogum passando os caminhos
#variavel de ambiente que define a pasta estatica de todos os trem de javascript, arquivo css são atendidos.
ENV STATIC_URL /static      
ENV STATIC_PATH /var/www/app/static

#copiar da sua maquina e jogar o container pegando sempre os caminhos com ogum
COPY ./requirements.txt /var/www/requirements.txt
COPY . /var/www


#mais um run pra executa a instalaçãp do pip e rodar meu requirements
RUN pip install -r /var/www/requirements.txt

