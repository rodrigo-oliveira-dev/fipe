SDK não oficial para a API da FIPE (http://fipeapi.appspot.com/)

# Como utilizar

## Instalação

```sh
    $ npm install --save fipe
```

## Realizando buscas

### Marcas

Buscar todas as marcas de carro disponíveis

```sh
    var fipeSdk = require('fipe').sdk;
    
    fipeSdk.brand('car')
        .all()
        .then(function(res) { 
            console.log(res); 
         });     
```

Buscar todas as marcas de caminhões disponíveis

```sh
    var fipeSdk = require('fipe').sdk;
    
    fipeSdk.brand('truck')
        .all()
        .then(function(res) { 
            console.log(res); 
        });
```

Buscar todas as marcas de motocicletas disponíveis

```sh
    var fipeSdk = require('fipe').sdk;
    fipeSdk.brand('motorcycle')
        .all()
        .then(function(res) { 
            console.log(res); 
        });
```

Buscar uma marca específica de carro

```sh
    var fipeSdk = require('fipe').sdk;
    
    fipeSdk.brand('car', 'fiat')
        .then(function(res) { 
            console.log(res); 
        });
```
ou 

```sh
    var fipeSdk = require('fipe').sdk;
    
    fipeSdk.brand('car')
        .findOneBy('name', 'volkswagen')
        .then(function(res) { 
            console.log(res); 
        });
```

### Veículos

Buscar todos os modelos de uma marca de carro específica

```sh
    var fipeSdk = require('fipe').sdk;
    
    fipeSdk.vehicle('car', 'subaru')
        .all()
        .then(function(res) { 
            console.log(res); 
        });
```

Buscar todas as ocorrências de um modelo de carro 

```sh
    var fipeSdk = require('fipe').sdk;
    
    fipeSdk.vehicle('car', 'chevrolet')
        .findBy('name', 'Celta')
        .then(function(res) { 
            console.log(res); 
        });    
```