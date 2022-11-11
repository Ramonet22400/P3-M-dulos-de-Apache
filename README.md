## P3: Módulos de Apache 

### 1. Añade en tu servidor el módulo mod_info y explique para que se utiliza este plugin.

*Este módulo nos va a permitir ver la información de nuestro servidor de forma remota a través de una página HTML.*

En esta imagen podemos ver los modúlos que vienen por defecto y estan isntalados en el apache2.

![image](https://user-images.githubusercontent.com/113515330/200918175-d0f537af-53fc-4bb1-ab98-7e8b224aec23.png) 

Gracias al comando "ls /etc/apache2/mods-available", podemos ver el mod_info.

![image](https://user-images.githubusercontent.com/113515330/200918645-dc50052d-cab0-4edd-abce-2dd04cb1c073.png)

Y mediante el siguiente comando lo habilitaremos en el apache2

![image](https://user-images.githubusercontent.com/113515330/200919012-b3bd305b-5962-4f62-8e38-ebc097be160a.png)

Volvemos a ver los mods habilitados y vemos que info a sido habilitado correctamente.

![image](https://user-images.githubusercontent.com/113515330/200919316-098ca20d-cc45-44ab-8af2-a13bc97315ab.png)


### 2. Oculta la versión del sistema y sistema de apache.

*Esto es interesante de hacer ya que previene dar información sobre nuestro servidor y sistema, un capa de seguridad digamos*

Primero de todo accederemos a security.conf, en donde están las dos características. 

![image](https://user-images.githubusercontent.com/113515330/200922651-50f3cc16-90ed-47b1-aa9e-974085bbfbce.png)

Una vez dentro cmabiaremos su configuración, aplicando los siguientes cambios: 

![image](https://user-images.githubusercontent.com/113515330/200922967-7bde31f5-0b61-4a27-bbf2-1a47dcc8894e.png)

Guardaremos y reinicamos el servidor Apache: sudo service apache2 restart


### 3. Crea una carpeta en la raíz del path del servidor con el nombre public y otra con el 
### nombre private. Permite que la carpeta public se visualice y el resto de las carpetas 
### que se creen, incluyendo private, no se muestren. A continuación, puede observar 
### como se debe de mostrar la carpeta public:

Primero de todo tendremos que acceder a la carpeta pública de Apache, y para movernos a traves de ella necesitaremos el siguiente comando: 

![image](https://user-images.githubusercontent.com/113515330/201221483-62312a49-11b8-4328-a7b3-f9f952c3db07.png)

Lo siguiente es crear un directorio, entonces para ello crearemos una carpeta con el nombre del directorio.

![image](https://user-images.githubusercontent.com/113515330/201221774-9c643a29-c10d-4fdc-a12d-a25f7cb5d297.png)

Luego crearemos la segunda carpeta, con el siguiente directorio.

![image](https://user-images.githubusercontent.com/113515330/201221884-f0cb3483-af7a-42d2-a90d-456b9ad6dfdd.png)

A continuación le daremos permiso a las dos carpetas, de esta forma evitaremos futuros problemas...

![image](https://user-images.githubusercontent.com/113515330/201222144-fc661460-e43f-4a9a-8404-deb6272ba0e8.png)

Reiniciaremos el Apache con: systemctl restart apache2. Y luego veremos que el directorio se ve tal que asi:

![image](https://user-images.githubusercontent.com/113515330/201305960-1603135c-7286-4537-a786-a9e4a5f9ce1a.png)


Las dos paginas se veran que ver de la siguiente forma una vez creadas:

![image](https://user-images.githubusercontent.com/113515330/201226816-a6f73f67-c868-4d65-8a8a-ccf4e5018c0f.png)

Como la segunda es una carpeta privada tendremos que tener permiso para acceder a ella.

![image](https://user-images.githubusercontent.com/113515330/201226847-cfd741f7-3741-4936-a917-4a87867a941d.png)



### 4. Prueba de acceder poniendo www. delante de tu URL actual. ¿Funciona? En caso  negativo, haz que funcione mediante el módulo mod_rewrite. Investigue como utilizar el archivo .htacess para implementarlo.


No hace falta ningún tipo de configuración ya esta por defecto.

![image](https://user-images.githubusercontent.com/113515330/201292018-d9983dad-9082-4ec5-af22-8a67783404ec.png)


### 5.Muestra los directorios de Apache con un tema diferente. Puedes utilizar 
###  https://github.com/ramlmn/Apache-Directory-Listing u otra alternativa que te llame la 
###    atención.

Tendremos que seguir los comandos y las instrucciones del link superior, y luego tendremos que cambiar el siguiente archivo:

![image](https://user-images.githubusercontent.com/113515330/201307977-46f41854-1f8f-4be5-a44a-2809291d9d25.png)

El resultado es el siguiente:

![image](https://user-images.githubusercontent.com/113515330/201308090-b1bb5a84-bbd0-42ea-b1b4-ae63bc0d2581.png)

### (Extra: 1 punto) Crea tu propio tema para el ejercicio anterior, sin dependencias 
### externas





