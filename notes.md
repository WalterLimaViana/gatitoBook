# Notes

## Aqui estará descrito o passo a passo de cada parte do projeto, como forma de aprendizado para projetos futuros.

## Criando o projeto

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

É possivel abreviar os comandos do angular colocando somente a primeira letra, como por exemplo ao invé de digitar ng generate component, colocamos apenas ng g c e completar com o nome do component.
ng g c home

### Criando o layout do home.component.html

Criado a estrutra da página principal.

## Criando a página Login

### Criando os components

A página login vai ser criada dentro da página home através do comando:
ng g c home/login

### Criando o layout

No arquivo login.component.html é criado o layout da página login utilizando o bootstrap como style.

## Criando a Autenticação do projeto

### Criado o módulo de autenticação

- Primeiro passo é criar o módulo:
  ng g m autenticacao

- Depois o service:
  ng g s autenticacao/autenticacao

- Dentro do autenticacao.serevice/ts instanciar o httpClient dentro do constructor
  constructor(private httpClient:Http:Client) através do import { HttpClient } from '@angular/common/http';

- Criar o método auntenticar, utilizando um Observable, que nesse casso utilizará um '<any>':
  autenticar(usuario:string, senha:string)
  ele vai retornar o return this.httpClient.post, passando a url ('http://localhost:3000/user/login',)
  com os atributos:
  userName: usuario,
  password: senha,

No arquivo login.component.html são feitas algumas mudanças:

- Adicionado o ngSubmit que vai chamar o método login dentro do form;
- Adicionado o ngModel dentro do input com a váriavel usuario e senha e no name usuario e senha;

No arquivo login.component.ts foram incluidos:

- as váriaveis usuario e senha que retornam vazio;
- o método login que é chamado no component.html, composto no momento somente por duas funções console.log apenas para mostrar o que foi digitado dentro do input após feito o submit na página.
