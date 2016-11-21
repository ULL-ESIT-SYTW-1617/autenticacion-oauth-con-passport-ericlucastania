#Práctica: Autentication


## Descripción

Esta práctica consiste en añadir la funcionalidad de poder acceder al libro si eres usuario de la organización. Si no eres usuario de la organización 
no podrás acceder al contenido del libro.




## Pasos a ejecutar 

**1. Instala nuestro paquete de forma global**

```npm install -g gitbook-start-elt```


**2. Ejecuta el binario para el render del template**
	
Tienes la opción de crear el repositorio o la opción de no crearlo:
	
	
**Crear repositorio**
* Si quieres que te cree un repositorio en Github tienes que poner la opción --repo "nombre repo"
	
   ```gitbook-start --dir Carpeta --repo```

Cuando ejecutes el paso anterior si no es la primera vez que lo haces te pedirá el usuario y 
		contraseña de github.Si introduces los datos correctamente te pedirá que introduzcas el nombre que quieres ponerle al repo,
		Ahora se desplegará el libro en github:
				
Ejemplo de uso:
				
				
![](https://4.bp.blogspot.com/-tZyZ4yGuI9A/WCxV2cB2ktI/AAAAAAAAAAg/I2tzZnB7FL4Nld6OQRs2NYG-SRwa9kIuwCLcB/s1600/repo.PNG)
				
Una vez que se te creado el repo ya puedes trabajar en él,ya no tendrás que poner más el 
			usuario y contraseña gracias a que se te generó un token para evitar que cada vez que quieras 
				crear un repo te pida tus credenciales.
				El token que se genera se guarda en el ./gitbook-start/config.json un lugar seguro para que no pueda acceder nadie
				que no seas tu.		

**No Crear repositorio**
* Si no quieres que se te cree el repositorio en Github simplemente ejecuta la siguiente opción
		
     ```gitbook-start --dir Carpeta``` !!Si no ejecutas el --dir se creará una carpeta con tu nombre de usuario

**3. Entra en la carpeta**

 ```cd Carpeta```




## PLUGINS

**1. Instala el plugin forma global**

```npm install -g gitbook-start-plugin-heroku-ericlucastania```

**2. Ejecuta el plugin que desees, asegúrate de estar dentro de la carpeta**


```gitbook-start -d heroku``` !! También puedes usar la opción --deploy


* Te pedirá un token, puedes generarlo ejecutando ```heroku auth:token``` o bien usar uno ya generado.
* Se te solicitará el nombre que tendrá tu aplicación en Heroku.
* Te preguntará si deseas pedir autentificación para que sólo los usuarios de tu organización puedan leer el libro.
   * Tienes diferentes opciones:
        * Si quieres que solo los usuarios de la organización puedan acceder al libro 
          tendras que poner la opción 's' o 'S' o simplemente darle a enter
        * Si quieres que cualquiera pueda acceder al libro,tendrás que poner la opción 
          'n' o 'N'
        

**3. Ejecuta el gulp creado**

```gulp deploy-heroku```







## Explicación

Cunado se ejecuta el gitbook-start -d PLUGIN se te lanzará el initialize del módulo,
el initialize crea una tarea en el gulp para realizar el deploy. Además de guardarte el paquete
elegido en el package.json.

## Opciones

    gitbook-start [OPTIONS]
        -d nombre del directorio a crear node gitbook-star -d miDirectorio
        -a autor del libro a crear node gitbook-star -a AutorDelLibro
        -e email del autor del libro node gitbook-star -e eric.ramos.suarez@gmail.com
        -r repositorio github contra el que se va a trabajar -r nameRepo
        -v muestra la version del paquete gitbook-start -v
        -h muestra ayuda sobre las opciones disponibles
        --repo nombre_del_repositorio que quieres crear en Github


## Enlaces interesantes 
 
* [NPM](https://www.npmjs.com/package/gitbook-start-elt)
* [Repositorio de la práctica](https://github.com/ULL-ESIT-SYTW-1617/crear-repositorio-en-github-ericlucastania-1.git)
* [Descripción de la tarea campus](https://casianorodriguezleon.gitbooks.io/ull-esit-1617/content/practicas/practicagithubapi.html)
* [PLUGIN HEROKU](https://github.com/ULL-ESIT-SYTW-1617/gitbook-start-heroku-ericlucastania.git)
* [NPM PLUGIN HEROKU](https://www.npmjs.com/package/gitbook-start-plugin-heroku-ericlucastania)
* [PLUGIN IAAS](https://github.com/ULL-ESIT-SYTW-1617/gitbook-start-heroku-ericlucastania.git)
* [NPM PLUGIN IAAS](https://www.npmjs.com/package/gitbook-start-plugin-heroku-ericlucastania)



## Componentes del grupo de trabajo

* [Eric Ramos](https://github.com/alu0100786330)
* [Lucas Ruiz](https://github.com/alu0100785265)
* [Tania González](https://github.com/tania77)






