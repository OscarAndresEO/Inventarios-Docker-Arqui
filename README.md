#Documentacion tecnica

Proyecto realizado en vue 3 in vite


## Levantado a nivel de desarrollo
Para utilizar el proyecto a nivel de desarrollo ejecutar el comando 

`npm run dev`


##Docker
para la construcción utilizar comando

`docker build-t dockerize-vuejs-app`
- dockerize-vuejs-app

Para correr la imagen utilizando docker

`docker run -it -p 8080:8080 --rm -name dockerize-vuejs-app-1 dockerize-vuejs-app`

## dependencias

 -axios 1.5.1
 -vue 3.3.4
 -node >v16.17.1
 -tailwindcss 3.3.3


-docker run: ejecuta un nuevo contenedor
    - -it: abrir una sesión interactiva
    - -p: exponer los puertos del contenedor
    - --rm: borre el contenedor despues de que lo detengamos (ahorra espacio)
    - --name: el nombre del nuevo contenedor
    - -image: