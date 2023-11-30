<!DOCTYPE html>
<html>
  <head>
  <meta charset="utf-8"/>
  <title>criando o meu primeiro objeto </title>
  </head>
  <header>
    <h1>criando o meu primeiro objeto </h1>
  </header>
  <body>
    
    <?php
    
    require_once 'caneta.php';
    $caneta_azul = new caneta;
    $caneta_azul->modelo = "Bic Cistal";
    $caneta_azul->cor = "Azul";
    $caneta_azul->ponta = 0.5;
    $caneta_azul->carga = "75%";
    $caneta_azul->tampar();
    
    $status = 'Destampada';
    if(($caneta_azul->tampada != NULL) ||
       ($caneta_azul->tampada !=0)){
         $status = 'Tampada';
       }
    echo'<pre>';
    print_r("<h1>Modelo :".$caneta_azul->modelo.
    "<br/>cor  :" .$caneta_azul->cor.
    "<br/>ponta :".$caneta_azul->ponta.
    "<br/>carga :".$caneta_azul->carga.
    "<br/>status :".$status.
    "<h1>");
    echo'</pre>';
    
    ?>
    
   
  </body>
</html>
