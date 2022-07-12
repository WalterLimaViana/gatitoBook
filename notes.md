# Notes

## Aqui estará descrito o passo a passo de cada parte do projeto, como forma de aprendizado para projetos futuros.

## Criando o projetos projeto

npm i g @angular/cli
ng new nomedoprojeto -strict
selecionar se haverá routing ou não. nesse caso y
selecionar tipo de style. CSS puro, SCSS, entre outros.

## Instalação de componentes de estilos

### Bootstrap e font-awesome no terminal

npm i bootstrap font-awesome

### no arquivo angular.json

abaixo de style entre as linhas 29 e 33, inserir as seguintes linhas:

    “./node_modules/bootstrap/dist/CSS/bootstrap.min.CSS”
    “./node_modules/font-awesome/CSS/font-awesome.CSS”

## Criando a página Home

### Criando o modulo

ng generate module home --routing

### Criando o component home

è possivel abreviar os comandos do angular colocando somente a primeira letra, como por exemplo ao invé de digitar ng generate component, colocamos apenas ng g c e completr com o nome do component.
ng g c home

### Criando o layout do home.component.html

Criado a estrutra da página principal
