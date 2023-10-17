# TALLER 7:   CONSTRUIR UNA APLICACIÓN SEGURA
Se construye una aplicación con una arquitectura que incluye dos servicios, y que cumplen con los siguientes parametros:
1. Debe permitir un acceso seguro desde el browser a la aplicación. Es decir debe garantizar autenticación, autorización e integridad de usuarios.
2. Debe tener al menos dos computadores comunicacndose entre ellos y el acceso de servicios remotos debe garantizar: autenticación, autorización e integridad entre los servicios. Nadie puede invocar los servicios si no está autorizado.
3. Desplegar el experimento en AWS. 

---
### Arquitectura
<img width="461" alt="image" src="https://github.com/CamiloCanta/AREP_lab7/assets/108955358/92b1e432-6602-436a-8253-31b8723be297">


---
### Prerrequisitos
Para elaborar este proyecto requerimos de las siguientes tecnologías:

 - Maven
 - Git
 - AWS
 - Java
---

### Instalación
instalamos Java, git y maven en nuestras instancias EC2

	 sudo yum install java-17-amazon-corretto.x86_64

  <img width="763" alt="image" src="https://github.com/CamiloCanta/AREP_lab7/assets/108955358/d093f410-68f3-4e6e-b40b-f8f16f8098e9">

  

  ```
  sudo yum install git -y
  ```
  ```
  sudo yum install maven -y
  ```
Clonamos el repositorio

     git clone https://github.com/CamiloCanta/AREP_lab7.git
    
Se accede al repositorio que acabamos de clonar

	 cd AREP_lab7

Antes de hacer la construcción del proyecto debemos realizar el ajuste de cambiar la direccion ip en la instancia que tiene el login para que haga una redireccion a la instancia que tiene el servicio cuando se inicia la sesión

Tambien debemos abrir los puertos en las instancias.

<img width="765" alt="image" src="https://github.com/CamiloCanta/AREP_lab7/assets/108955358/e4d769bd-474a-4832-aff3-9bd21f1db12b">


Hacemos la construcción del proyecto

	 mvn clean package install
---

### Corriendo
Una vez creadas las instancias

<img width="769" alt="image" src="https://github.com/CamiloCanta/AREP_lab7/assets/108955358/c8b699d7-4c20-4034-a867-11b62c9be75b">


Se clona el repositorio donde alojamos el proyecto
	
     git clone https://github.com/CamiloCanta/AREP_lab7.git

y nos posicionamos en la carpeta root del proyecto

	 cd AREP_lab7

una vez aquí debemos levantar el servicio que le corresponde a cada instancia EC2

	 java -cp "target/classes:target/dependency/*" eci.escuelaing.edu.co.apps.LoginApp

<img width="724" alt="image" src="https://github.com/CamiloCanta/AREP_lab7/assets/108955358/99e21836-73bb-4007-a9ca-56c3c3c51f73">


  
	 java -cp "target/classes:target/dependency/*" eci.escuelaing.edu.co.apps.BasicApp

<img width="725" alt="image" src="https://github.com/CamiloCanta/AREP_lab7/assets/108955358/08f7cf5e-0fef-4809-a732-6230c66fc455">


### Video Demo

**[video](https://youtu.be/VusHV8OsLS8?si=3imnlW4IFEjPF956)**

Usuario registrado
- camilo -> camilo123


	
---
## Construido con

* [Maven](https://maven.apache.org/): Apache Maven es una herramienta que estandariza la configuración de un proyecto en todo su ciclo de vida.
* [Git](https://rometools.github.io/rome/):  Es un sistema de control de versiones distribuido (VCS).
* [IntelliJ](https://www.jetbrains.com/idea/): Es un entorno de desarrollo integrado para el desarrollo de programas informáticos.
* [Java 19](https://www.java.com/es/): Lenguaje de programación de propósito general, es decir, que sirve para muchas cosas, para web, servidores, aplicaciones móviles, entre otros. Java también es un lenguaje orientado a objetos, y con un fuerte tipado de variables.
* [Html](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/HTML_basics): Es el código que se utiliza para estructurar y desplegar una página web y sus contenidos.
* [JavaScript](https://developer.mozilla.org/es/docs/Learn/JavaScript/First_steps/What_is_JavaScript): JavaScript es un lenguaje de programación o de secuencias de comandos que te permite implementar funciones complejas en páginas web
* [CSS](https://developer.mozilla.org/es/docs/Learn/CSS/First_steps/What_is_CSS): Las hojas de estilo en cascada permiten crear páginas web atractivas.
* [AWS](https://www.inbest.cloud/comunidad/qu%C3%A9-es-aws): Amazon Web Services es una plataforma de servicios de nube que te ofrece potencia de cómputo, almacenamiento de bases de datos, entrega de contenido y otra funcionalidad para ayudar a tu negocio a escalar y crecer

## Autor
- **[Camilo Andres Cantillo Tatis](https://www.linkedin.com/in/camilocanta/)** 
