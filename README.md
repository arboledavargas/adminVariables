# Documentacion API administrador de variables


Esta es la documentacion del proyecto administrador de variables, esta contruido como una API REST. A continuacion se alistan los diferentes Endpoints:

## Endpoints:

###  aplicaciones 

url: /api/applications

---

Descripcion: Listar aplicaciones

Metodo: GET 

respuesta:   

 ```json
 {
    "data": [
        {
            "id": "0",
            "nombre": "example",
            "entorno": "desarrollo",
            "variables": {
                "variable1": "valor1",
                "variable2": "valor2",
            }
        },
        
        {
            "id": "1",
            "nombre": "example",
            "entorno": "produccion",
            "variables": {
                "variable1": "valor1",
                "variable2": "valor2",
            }   
        }
    ] 
}
 
 ```
---
Descripcion: crear aplicacion

 metodo: POST 

body: 

```json
{
    "nombre": "example",
    "entorno": "desarrollo",
    "variables": {
        "variable1": "valor1",
        "variable2": "valor2",
    }
}
```

respuesta:
```json
{
    "id": "3",
    "nombre": "example",
    "entorno": "desarrollo",
    "variables": {
        "variable1": "valor1",
        "variable2": "valor2",
    }
}
```
---
## Unica aplicacion


url: /api/applications/:idAplicacion



---
Descripcion: actualizar aplicacion
 

metodo: PUT

body:

```json
{
    "nombre": "example",
    "entorno": "desarrollo",
    "variables": {
        "variable1": "valor1",
        "variable2": "valor2",
    }
}
```
respuesta:
```json
{
    "id": "2",
    "nombre": "example",
    "entorno": "desarrollo",
    "variables": {
        "variable1": "valor1",
        "variable2": "valor2",
    }
}
```
---


Descripcion: eliminar elemento

metodo: DELETE

respuesta: 

```json
{
     "msg": "Everything ok",
    
}
```


