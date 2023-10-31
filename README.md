# PARCIAL_1_MMN
# 1) Explica que es un “Pull Request” en Github
Un pull request se realiza al clonar el repositorio de otra persona, realizar cambios en él y querer fusionar tus cambios dentro de su repositorio remoto. Primero hay que hacer un push de tus cambios desde el local hasta el repositorio clonado, después, desde Github, darle al botón CREATE PULL REQUEST para que le llegue a la persona que creó el repositorio original.
# 2) ¿Qué es un conflicto de fusión (merge conflict) en Git? Explica como resolverías este conflicto.
Un conflicto de fusión ocurre cuando creas una nueva rama (a partir de un commit, por ejemplo) y realizas cambios en el fichero/s. Al fusionar con la rama original, hay líneas cambiadas (de orden, de contenido...) y git lo detecta como error. Para solucionarlo, sólo hay que volver a entrar en el archivo/s, borrar las líneas que no estaban anteriormente (<<<<<, >>>>>, ======), volver a añadir los cambios al staging con git add y hacer un commit para dejar rastro de ello.
# 3) Imaginemos que tenemos dos ramas, la principal llamada “main” y la rama “examen_parcial”. ¿Qué procedimiento se debería seguir para fusionar (merge) ambas ramas? 
Si estamos en la rama "examen_parcial", nos quedamos ahí. Hacemos git merge main para integrar los cambios de la rama principal a la rama en la que estamos (examen_parcial). Surgirán conflictos, que se resuelven editando los ficheros, borrando las líneas de conflicto, haciendo git add . y un commit para cada cambio. Al hacer esto, hacemos git checkout main para movernos a la rama main y git merge examen_parcial para integrar todo a la rama principal.
# 4) Has realizado un commit, pero luego descubres un error importante en los cambios que has incluido. Necesitas revertir este último commit para regresar tu proyecto al estado anterior, pero deseas mantener los cambios realizados en tu área de trabajo. Explica el comando de Git que utilizarías para llevar a cabo esta acción.
Yo abriría el archivo donde se han creado los cambios que se quieren revertir; manteniendo los cambios realizados en mi área de trabajo. Volvería a editar el archivo a como estaba antes. Saldría del editor, añadiría los cambios al staging con git add . y crearía un nuevo commit que describa que se han revertido los cambios anteriores.

# 5) ¿Cómo se realiza un fork de un repositorio en GitHub y para qué se utiliza comúnmente esta acción?
Entrando en el repositorio y darle al botón de fork. Después, desde la consola se hace git clone con la url del repositorio para clonarlo. Se utiliza para clonar un repositorio y trabajar en él estando ya creado.
# 6) Te encuentras trabajando en un proyecto y necesitas llegar a un archivo específico llamado "archivo.txt". Este archivo está ubicado dentro de una estructura de directorios en tu sistema.
a) Usando el comando cd. --> cd Nombre_del_alumno  cd Universidad  cd UAX y otra vez cd al directorio que contiene "archivo.txt". RUTA ABSOLUTA (desde el directorio raiz)
b) cd UAX y cd al directorio que contiene "archivo.txt". RUTA RELATIVA (desde un lugar de referencia específico)
# 7)
1)git clone  
2)git branch  
3)git checkout  
4)git add  
5)git commit  
6)git push  
7)git pull
8)git merge  
9)git reset -hard 
10)git log
# 8) 
Primero me movería a la rama 'matemáticas' usando el comando git checkout matemáticas. Después, integraría el contendido de 'develop' en matemáticas, para tener todos los cambios en la rama, usando git merge develop. Surgirán conflictos, podemos verlos haciendo git status. Para resolverlos, abrimos los archivos uno por uno. En cada uno, se hace git add . para añadir los cambios al staging y se realiza un commit con un mensaje significativo (git commit -m "Update archivo.txt"). Ahora podemos hacer git merge --continue y al resolverlos ya se habrán mergeado las ramas. Entramos en la rama develop con git checkout develop y ahora sí integramos la rama matemáticas en develop con git merge matemáticas. Ahora, se repite el proceso con la rama diseño-UX. Nos movemos a la rama 'diseño-UX' usando el comando git checkout diseño-UX. Después, integraría el contendido de 'develop' en 'diseño-UX', para tener todos los cambios en la rama, usando git merge develop. Surgirán conflictos, podemos verlos haciendo git status. Para resolverlos, abrimos los archivos uno por uno. En cada uno, se hace git add . para añadir los cambios al staging y se realiza un commit con un mensaje significativo (git commit -m "Update archivo.txt"). Ahora podemos hacer git merge --continue y al resolverlos ya se habrán mergeado las ramas. Entramos en la rama develop con git checkout develop y ahora sí integramos la rama diseño-UX en develop con git merge diseño-UX. Ahora todos los cambios están en develop.

# 9) ¿Cuál de las siguientes afirmaciones describe mejor el proceso que seguiste para añadir el botón de "x^4" a tu calculadora web y subir los cambios al repositorio remoto?
C) Añadiste el botón "x^4" al archivo "index.html" en tu repositorio local, creaste un commit con los cambios y luego subiste el repositorio local al remoto en la rama principal (master).
