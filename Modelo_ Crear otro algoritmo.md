# **Modelo: Crear otro algoritmo**

##  **Introducción¶**

Una parte importante de la ciberseguridad es controlar el acceso al contenido restringido. En este laboratorio, trabajarás con un archivo de texto que contiene direcciones IP a las que se les permite acceder a contenido restringido específico de tu organización.

El análisis de un archivo permite a los analistas de seguridad leer y actualizar el contenido. Python ayuda a los analistas a desarrollar algoritmos para automatizar el proceso de analizar archivos y mantenerlos actualizados.

Desarrollarás un algoritmo que analice este archivo de texto de direcciones IP y lo actualice eliminando las direcciones que ya no tienen acceso al contenido restringido.

## **Consejos para completar este laboratorio**

## **Situación hipotética**

En este laboratorio, trabajarás como analista de seguridad y serás responsable de desarrollar un algoritmo que analice un archivo que contiene direcciones IP a las que se les permite acceder a contenido restringido y elimine las direcciones que ya no tienen acceso.

##  **Tarea 1**

Tu objetivo final es desarrollar un algoritmo que analice una serie de direcciones IP que pueden acceder a información restringida y elimine aquellas que ya no pueden hacerlo. Python puede automatizar este proceso.

Se te proporciona un archivo de texto llamado `"allow_list.txt"` que contiene una serie de direcciones IP a las que se les permite acceder a información restringida.

**Nota**: En la actividad, el valor de la cadena import\_file es `"allow_list.txt"`, pero en el modelo es `"data/allow_list.txt"`. Esto es intencional. En el modelo, se movió una copia única de `"allow_list.txt"` a una carpeta nueva para que los cambios realizados en el archivo de la actividad no afecten al archivo utilizado en el modelo.

Hay direcciones IP que ya no deberían tener acceso a esta información y es necesario eliminarlas del archivo de texto. Se te proporciona una variable llamada `remove_list` que contiene la lista de direcciones IP que es necesario eliminar.

Muestra ambas variables para explorar su contenido y ejecuta la celda. Asegúrate de reemplazar cada `### TU CÓDIGO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda.  
In \[1\]:  
*\# Asigna a \`import\_file\` el nombre del archivo*

import\_file \= "data/allow\_list.txt"

*\# Asigna a \`remove\_list\` una lista de direcciones IP a las que ya no se les permite acceder a información restringida.* 

remove\_list \= \["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"\]

*\# Muestra \`import\_file\`*

print(import\_file)

*\# Muestra \`remove\_list\`*

print(remove\_list)

data/allow\_list.txt  
\['192.168.97.225', '192.168.158.170', '192.168.201.40', '192.168.58.57'\]

#### **Pista 1**

#### **Pregunta 1**

**¿Qué observas de la salida anterior?**  
La primera línea de la salida muestra el nombre del archivo de texto. La segunda línea de la salida muestra la lista de direcciones IP de `remove_list`.

## **Tarea 2**

En esta tarea, comienza por abrir el archivo de texto con la variable `import_file`, la palabra clave `with` y la función `open()` con el parámetro `"r"`. Asegúrate de reemplazar `### TU CÓDIGO AQUÍ ###` con tu propio código. Por ahora, escribirás la primera línea de la sentencia `with`. La ejecución de este código producirá un error, ya que solo contendrá la primera línea de la sentencia `with`; completarás esta sentencia `with` en la tarea después de esto.  
In \[2\]:  
*\# Asigna a \`import\_file\` el nombre del archivo*

import\_file \= "data/allow\_list.txt"

*\# Asigna a \`remove\_list\` una lista de direcciones IP a las que ya no se les permite acceder a información restringida.* 

remove\_list \= \["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"\]

*\# La primera línea de la sentencia \`with\`*

**with** open(import\_file, "r") **as** file:

\[0;36m  File \[0;32m"\<ipython-input-2-570da020cff3\>"\[0;36m, line \[0;32m11\[0m  
\[0;31m    with open(import\_file, "r") as file:\[0m  
\[0m                                        ^\[0m  
\[0;31mSyntaxError\[0m\[0;31m:\[0m unexpected EOF while parsing

#### **Pista 1**

##  **Tarea 3**

Ahora usa el método `.read()` para leer el archivo importado y almacenarlo en una variable llamada `ip_addresses`.

Luego, muestra `ip_addresses` para examinar los datos en su formato actual.

Asegúrate de reemplazar cada `### TU CÓDIGO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda.  
In \[4\]:  
*\# Asigna a \`import\_file\` el nombre del archivo*

import\_file \= "data/allow\_list.txt"

*\# Asigna a \`remove\_list\` una lista de direcciones IP a las que ya no se les permite acceder a información restringida.* 

remove\_list \= \["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"\]

*\# Crea la sentencia \`with\` para leer el contenido inicial del archivo*

**with** open(import\_file, "r") **as** file:

  *\# Usa \`.read()\` para leer el archivo importado y almacenarlo en una variable llamada \`ip\_addresses\`*

    ip\_addresses \= file.read()

*\# Muestra \`ip\_addresses\`*

print(ip\_addresses)

ip\_address 192.168.25.60 192.168.205.12 192.168.6.9 192.168.52.90 192.168.90.124 192.168.186.176 192.168.133.188 192.168.203.198 192.168.218.219 192.168.52.37 192.168.156.224 192.168.60.153 192.168.69.116

#### **Pista 1**

#### **Pista 2**

#### **Pista 3**

#### **Pregunta 2**

**¿Alguna de las direcciones IP de la lista de permisos también está en `remove_list`?**  
Hay cuatro direcciones IP en la lista de permisos que también están en `remove_list`.

## **Tarea 4**

Después de leer el archivo, vuelve a asignar la variable `ip_addresses` para actualizar el tipo de datos de una cadena a una lista. Para hacerlo, usa el método `.split()`. Si añades este paso, después podrás eliminar direcciones IP de la lista de permisos.

Luego, muestra la variable `ip_addresses` para verificar que se actualizó.

Asegúrate de reemplazar cada `### TU CÓDIGO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda.  
In \[5\]:  
*\# Asigna a \`import\_file\` el nombre del archivo*

import\_file \= "data/allow\_list.txt"

*\# Asigna a \`remove\_list\` una lista de direcciones IP a las que ya no se les permite acceder a información restringida.* 

remove\_list \= \["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"\]

*\# Crea la sentencia \`with\` para leer el contenido inicial del archivo*

**with** open(import\_file, "r") **as** file:

  *\# Usa \`.read()\` para leer el archivo importado y almacenarlo en una variable llamada \`ip\_addresses\`*

    ip\_addresses \= file.read()

*\# Usa \`.split()\` para convertir \`ip\_addresses\` de una cadena a una lista*

ip\_addresses \= ip\_addresses.split()

*\# Muestra \`ip\_addresses\`*

print(ip\_addresses)

\['ip\_address', '192.168.25.60', '192.168.205.12', '192.168.6.9', '192.168.52.90', '192.168.90.124', '192.168.186.176', '192.168.133.188', '192.168.203.198', '192.168.218.219', '192.168.52.37', '192.168.156.224', '192.168.60.153', '192.168.69.116'\]

#### **Pista 1**

#### **Pista 2**

##  **Tarea 5**

Ahora, escribirás un código que elimine los elementos de `remove_list` de la lista `ip_addresses`. Necesitarás usar una sentencia iterativa.

Primero, crea la sentencia iterativa. Nombra la variable de bucle `element` que recorre en bucle `remove_list` y muestra cada elemento. Asegúrate de reemplazar cada `### TU CÓDICO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda.  
In \[6\]:  
*\# Asigna a \`import\_file\` el nombre del archivo*

import\_file \= "data/allow\_list.txt"

*\# Asigna a \`remove\_list\` una lista de direcciones IP a las que ya no se les permite acceder a información restringida.*

remove\_list \= \["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"\]

*\# Crea la sentencia \`with\` para leer el contenido inicial del archivo*

**with** open(import\_file, "r") **as** file:

  *\# Usa \`.read()\` para leer el archivo importado y almacenarlo en una variable llamada \`ip\_addresses\`*

    ip\_addresses \= file.read()

*\# Usa \`.split()\` para convertir \`ip\_addresses\` de una cadena a una lista*

ip\_addresses \= ip\_addresses.split()

*\# Crea una sentencia iterativa*  
*\# Nombra la variable de bucle \`element\`*  
*\# Recorre en bucle \`remove\_list\`*

**for** element **in** remove\_list:

  *\# Muestra \`element\` en cada iteración*

    print(element)

192.168.97.225  
192.168.158.170  
192.168.201.40  
192.168.58.57

#### **Pista 1**

#### **Pista 2**

## **Tarea 6**

Ahora, en el cuerpo de la sentencia iterativa, aplica el método `.remove()` a la lista `ip_addresses` y elimina las direcciones IP identificadas en la variable de bucle `element`.

Después de que la sentencia iterativa elimina los elementos, muestra la lista `ip_addresses` actualizada para comprobar que los elementos de `remove_list` ya no están en `ip_addresses`. Asegúrate de reemplazar cada `### TU CÓDICO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda.

No olvides las dos cualidades de las listas que hacen posible la aplicación del método `.remove()`. Primero, todos los elementos en `remove_list` también están en la lista `ip_addresses`. Si no fuera así, aplicar el método `.remove()` a estos elementos generaría un error. En segundo lugar, no hay valores duplicados en la lista `ip_addresses`. El método `.remove()` solo elimina la primera aparición de un elemento, por lo que si hubiera valores duplicados, no se eliminarían.  
In \[ \]:  
*\# Asigna a \`import\_file\` el nombre del archivo*

import\_file \= "data/allow\_list.txt"

*\# Asigna a \`remove\_list\` una lista de direcciones IP a las que ya no se les permite acceder a información restringida.*

remove\_list \= \["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"\]

*\# Crea la sentencia \`with\` para leer el contenido inicial del archivo*

**with** open(import\_file, "r") **as** file:

  *\# Usa \`.read()\` para leer el archivo importado y almacenarlo en una variable llamada \`ip\_addresses\`*

    ip\_addresses \= file.read()

*\# Usa \`.split()\` para convertir \`ip\_addresses\` de una cadena a una lista*

ip\_addresses \= ip\_addresses.split()

*\# Crea una sentencia iterativa*  
*\# Nombra la variable de bucle \`element\`*  
*\# Recorre en bucle \`remove\_list\`*

**for** element **in** remove\_list:

  *\# usa el método \`.remove()\` para eliminar*  
  *\# elementos de \`ip\_addresses\`*

    ip\_addresses.remove(element)

*\# Muestra \`ip\_addresses\`*

print(ip\_addresses)

#### **Pista 1**

#### **Pista 2**

## **Tarea 7**

El paso siguiente es actualizar el archivo original que se usó para crear la lista `ip_addresses`. Se agregó una línea de código que contiene el método `.join()` para que el archivo se pueda actualizar. Esto es necesario porque `ip_addresses` debe estar en formato de cadena cuando se usa dentro de la sentencia `with` para reescribir el archivo.

El método `.join()` toma un elemento iterable (como una lista) y concatena cada uno de sus elementos en una cadena. Se aplica el método `.join()` a una cadena que consiste en el carácter que se usará para separar cada elemento en el iterable una vez que se convierta en una cadena. En el siguiente código, se aplica el método a la cadena `" "`, que contiene solo un carácter de espacio. El argumento del método `.join()` es el iterable que deseas convertir que, en este caso, es `ip_addresses`. Como resultado, vuelve a convertir la lista `ip_addresses` en una cadena con un espacio entre cada elemento.

Después de la línea con el método `.join()`, crea la sentencia `with` que reescribirá el archivo original. Usa el parámetro `"w"` cuando necesites llamar a la función `open()` para eliminar el contenido del archivo original y reemplazarlo con lo que quieras escribir. Asegúrate de reemplazar cada `### TU CÓDIGO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda. Esta celda de código no generará una salida.  
In \[ \]:  
*\# Asigna a \`import\_file\` el nombre del archivo*

import\_file \= "data/allow\_list.txt"

*\# Asigna a \`remove\_list\` una lista de direcciones IP a las que ya no se les permite acceder a información restringida.*

remove\_list \= \["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"\]

*\# Crea la sentencia \`with\` para leer el contenido inicial del archivo*

**with** open(import\_file, "r") **as** file:

  *\# Usa \`.read()\` para leer el archivo importado y almacenarlo en una variable llamada \`ip\_addresses\`*

    ip\_addresses \= file.read()

*\# Usa \`.split()\` para convertir \`ip\_addresses\` de una cadena a una lista*

ip\_addresses \= ip\_addresses.split()

*\# Crea una sentencia iterativa*  
*\# Nombra la variable de bucle \`element\`*  
*\# Recorre en bucle \`remove\_list\`*

**for** element **in** remove\_list:

  *\# usa el método \`.remove()\` para eliminar*  
  *\# elementos de \`ip\_addresses\`*

    ip\_addresses.remove(element)

*\# Vuelve a convertir \`ip\_addresses\` en una cadena para que se pueda escribir en un archivo de texto*

ip\_addresses \= " ".join(ip\_addresses)

*\# Crea una sentencia \`with\` para reescribir el archivo original*

**with** open(import\_file, "w") **as** file:

  *\# Para reescribir el archivo, reemplaza su contenido con \`ip\_addresses\`*

    file.write(ip\_addresses)

#### **Pista 1**

#### **Pista 2**

#### **Pista 3**

## **Tarea 8**

En esta tarea, comprobarás que el archivo original se reescribió con la lista correcta.

Escribe otra sentencia `with`, esta vez para leer el archivo actualizado. Comienza abriendo el archivo. Luego, lee el archivo y guarda el contenido en la variable `text`.

Muestra la variable `text` para examinar el resultado.

Asegúrate de reemplazar cada `### TU CÓDIGO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda.  
In \[3\]:  
*\# Asigna a \`import\_file\` el nombre del archivo*

import\_file \= "data/allow\_list.txt"

*\# Asigna a \`remove\_list\` una lista de direcciones IP a las que ya no se les permite acceder a información restringida.*

remove\_list \= \["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"\]

*\# Crea la sentencia \`with\` para leer el contenido inicial del archivo*

**with** open(import\_file, "r") **as** file:

  *\# Usa \`.read()\` para leer el archivo importado y almacenarlo en una variable llamada \`ip\_addresses\`*

    ip\_addresses \= file.read()

*\# Usa \`.split()\` para convertir \`ip\_addresses\` de una cadena a una lista*

ip\_addresses \= ip\_addresses.split()

*\# Crea una sentencia iterativa*  
*\# Nombra la variable de bucle \`element\`*  
*\# Recorre en bucle \`remove\_list\`*

**for** element **in** remove\_list:

  *\# usa el método \`.remove()\` para eliminar*  
  *\# elementos de \`ip\_addresses\`*

    ip\_addresses.remove(element)

*\# Vuelve a convertir \`ip\_addresses\` en una cadena para que se pueda escribir en un archivo de texto*

ip\_addresses \= " ".join(ip\_addresses)

*\# Crea una sentencia \`with\` para reescribir el archivo original*

**with** open(import\_file, "w") **as** file:

  *\# Para reescribir el archivo, reemplaza su contenido con \`ip\_addresses\`*

    file.write(ip\_addresses)

*\# Crea la sentencia \`with\` para leer el archivo actualizado*

**with** open(import\_file, "r") **as** file:

  *\# Lee el archivo actualizado y almacena el contenido en \`text\`*

    text \= file.read()

*\# Muestra el contenido de \`text\`*

print(text)

\[0;31m---------------------------------------------------------------------------\[0m  
\[0;31mValueError\[0m                                Traceback (most recent call last)  
\[0;32m\<ipython-input-3-5ca175e506c2\>\[0m in \[0;36m\<module\>\[0;34m\[0m  
\[1;32m     28\[0m   \[0;31m\# elements from \`ip\_addresses\`\[0m\[0;34m\[0m\[0;34m\[0m\[0;34m\[0m\[0m  
\[1;32m     29\[0m \[0;34m\[0m\[0m  
\[0;32m---\> 30\[0;31m     \[0mip\_addresses\[0m\[0;34m.\[0m\[0mremove\[0m\[0;34m(\[0m\[0melement\[0m\[0;34m)\[0m\[0;34m\[0m\[0;34m\[0m\[0m  
\[0m\[1;32m     31\[0m \[0;34m\[0m\[0m  
\[1;32m     32\[0m \[0;31m\# Convert \`ip\_addresses\` back to a string so that it can be written into the text file\[0m\[0;34m\[0m\[0;34m\[0m\[0;34m\[0m\[0m

\[0;31mValueError\[0m: list.remove(x): x not in list

#### **Pista 1**

#### **Pista 2**

#### **Pista 3**

## **Tarea 9**

El paso siguiente es llevar todo el código que escribiste hasta este punto y ponerlo todo en una sola función.

Define una función llamada `update_file()` que recibe dos parámetros. El primer parámetro es el nombre del archivo de texto que contiene las direcciones IP (llama a este parámetro `import_file`). El segundo parámetro es una lista que contiene las direcciones IP a eliminar (llama a este parámetro `remove_list`).

Asegúrate de reemplazar `### TU CÓDIGO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda. Ten en cuenta que esta celda de código no generará ninguna salida.  
In \[ \]:  
*\# Define una función llamada \`update\_file\` que recibe dos parámetros: \`import\_file\` y \`remove\_list\`*  
*\# y combina los pasos que escribiste en este laboratorio hasta el momento*

**def** update\_file(import\_file, remove\_list):

  *\# Crea la sentencia \`with\` para leer el contenido inicial del archivo*

    **with** open(import\_file, "r") **as** file:

    *\# Usa \`.read()\` para leer el archivo importado y almacenarlo en una variable llamada \`ip\_addresses\`*

        ip\_addresses \= file.read()

  *\# Usa \`.split()\` para convertir \`ip\_addresses\` de una cadena a una lista*

    ip\_addresses \= ip\_addresses.split()

  *\# Crea una sentencia iterativa*  
  *\# Nombra la variable de bucle \`element\`*  
  *\# Recorre en bucle \`remove\_list\`*

    **for** element **in** remove\_list:

    *\# usa el método \`.remove()\` para eliminar*  
    *\# elementos de \`ip\_addresses\`*

        ip\_addresses.remove(element)

  *\# Vuelve a convertir \`ip\_addresses\` en una cadena para que se pueda escribir en un archivo de texto*

    ip\_addresses \= " ".join(ip\_addresses)

  *\# Crea una sentencia \`with\` para reescribir el archivo original*

    **with** open(import\_file, "w") **as** file:

    *\# Para reescribir el archivo, reemplaza su contenido con \`ip\_addresses\`*

        file.write(ip\_addresses)

#### **Pista 1**

#### **Pista 2**

#### **Pista 3**

#### **Pregunta 3**

**¿Cuáles son los beneficios de incorporar el algoritmo en una sola función?**  
La incorporación del algoritmo en una sola función ayuda a organizar el código y hacerlo reutilizable. Si quieres ejecutar el algoritmo más de una vez, lo que tienes que hacer es llamar a la función que lo contiene.

## **Tarea 10**

Finalmente, llama a la función `update_file()` que definiste. Aplica la función a `"allow_list.txt"` y pásale una lista de direcciones IP como segundo argumento.

Usa la siguiente lista de direcciones IP como segundo argumento:

`["192.168.25.60", "192.168.140.81", "192.168.203.198"]`

Después de llamar a la función, usa una sentencia `with` para leer el contenido de la lista de permisos. Luego, muestra el contenido de la lista de permisos. Ejecútalo para comprobar que la función actualizó el archivo.

Asegúrate de reemplazar `### TU CÓDIGO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda.  
In \[ \]:  
*\# Define una función llamada \`update\_file\` que recibe dos parámetros: \`import\_file\` y \`remove\_list\`*  
*\# y combina los pasos que escribiste en este laboratorio hasta el momento*

**def** update\_file(import\_file, remove\_list):

  *\# Crea la sentencia \`with\` para leer el contenido inicial del archivo*

    **with** open(import\_file, "r") **as** file:

    *\# Usa \`.read()\` para leer el archivo importado y almacenarlo en una variable llamada \`ip\_addresses\`*

        ip\_addresses \= file.read()

  *\# Usa \`.split()\` para convertir \`ip\_addresses\` de una cadena a una lista*

    ip\_addresses \= ip\_addresses.split()

  *\# Crea una sentencia iterativa*  
  *\# Nombra la variable de bucle \`element\`*  
  *\# Recorre en bucle \`remove\_list\`*

    **for** element **in** remove\_list:

    *\# usa el método \`.remove()\` para eliminar*  
    *\# elementos de \`ip\_addresses\`*

        ip\_addresses.remove(element)

  *\# Vuelve a convertir \`ip\_addresses\` en una cadena para que se pueda escribir en un archivo de texto*

    ip\_addresses \= " ".join(ip\_addresses)

  *\# Crea una sentencia \`with\` para reescribir el archivo original*

    **with** open(import\_file, "w") **as** file:

    *\# Para reescribir el archivo, reemplaza su contenido con \`ip\_addresses\`*

        file.write(ip\_addresses)

*\# Llama a \`update\_file()\` y pásale "allow\_list.txt" como argumento y una lista de las direcciones IP a eliminar*

update\_file("data/allow\_list.txt", \["192.168.25.60", "192.168.140.81", "192.168.203.198"\])

*\# Crea la sentencia \`with\` para leer el archivo actualizado*

**with** open("data/allow\_list.txt", "r") **as** file:

  *\# Lee el archivo actualizado y almacena el contenido en \`text\`*

    text \= file.read()

*\# Muestra el contenido de \`text\`*

print(text)

#### **Pista 1**

#### **Pista 2**

#### **Pista 3**

## **Conclusión**

**¿Qué conclusiones clave obtuviste de este laboratorio?**  
— Python tiene funciones y sintaxis que te ayudan a importar y analizar archivos de texto. — La sentencia `with` te permite gestionar archivos de manera eficiente. — La función `open()` te permite importar o abrir un archivo. Toma el nombre del archivo como primer parámetro y una cadena que indica el propósito de abrir el archivo como segundo parámetro. — Especifica `"r"` como segundo parámetro si quieres abrir el archivo con fines de lectura. — Especifica `"w"` como segundo parámetro si quieres abrir el archivo con fines de escritura. — El método `.read()` te permite leer un archivo. — El método `.write()` te permite agregar datos o escribir en un archivo. — Puedes usar un bucle `for` para recorrer en iteración una lista. — Puedes usar el método `.split()` para convertir una cadena en una lista. — Puedes usar Python para comparar el contenido de un archivo de texto con los elementos de una lista. — Se pueden incorporar algoritmos a las funciones. Al definir una función, debes especificar los parámetros que toma y las acciones que debe ejecutar.  
