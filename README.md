# Devyzi-Framework
Framework PHP sem fins lucrativos.

## Instalação
Para utilizar o Devyzi Framework execute o seguinte comando no composer:
```
composer create-project devyzi/devyzi nome-do-projeto
```
altere o 'pasta-do-projeto' para o nome do seu novo projeto.

Caso você ainda não tenha o composer instalado [clique aqui](https://getcomposer.org/doc/00-intro.md) e aprenda a instala-lo.

## Routes
Para criar rotas, vá até o arquivo localizado em 'App/Routes' e faça sua rota no seguinte formato:
```
$routes['nome-da-rota'] = array('route'=>'/rota','controller'=>"SeuArquivoController",'action'=>'SuaFunção');
```
## Controllers
Para criar um controller, você deve extende-lo de Action, segue o exemplo:
```
<?php
namespace App\Controllers;


use DEVYZI\Controller\Action;

class HomeController extends Action
{
    public function show()
    {
       $name = "Marcus Campos"
       $this->render("Home", $name); //Renderiza a view home
    }
}
```
## Models
Para criar um model, você deve extende-lo de Table, posteriormente declare uma variável 'protected $table' atribuindo como valor o nome da sua tabela no banco de dados, segue o exemplo:
```
<?php
namespace App\Models;


use DEVYZI\Model\Table;

class Client extends Table
{
    protected $table = "clientes";
}
```
## Views
Para criar uma view, você deve criar seu arquivo com a sequinte extensão '.blade.php', exemplo: 'Home.blade.php'.
Desta forma, a view terá suporte ao template blade, veja um exemplo de como usar o blade:
```
<h1>{{ $name }} </h1>
```

#Patrocine este projeto
Caso você goste e queira patrocinar este projeto, [clique aqui](https://www.patreon.com/user?u=3580444) e doe para que o desenvolvimento do framework possa ser acelerado.

![Devyzi Framework](http://i.imgur.com/Mffjnem.png)