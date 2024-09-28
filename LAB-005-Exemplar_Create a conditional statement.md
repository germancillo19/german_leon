# Modelo: Crea una sentencia condicional

## Introducción

Las sentencias condicionales son una estructura poderosa que ayuda a lograr la automatización cuando necesitas asegurarte de que se cumplan las condiciones antes de ejecutar ciertas acciones. Por ejemplo, los analistas de seguridad pueden usar sentencias condicionales en Python para verificar si los usuarios están autorizados a acceder a un dispositivo. 

En este laboratorio, practicarás escribiendo sentencias condicionales en Python.

<details><summary><h2>Consejos para completar este laboratorio</h2></summary>

Mientras recorres este laboratorio, ten en cuenta los siguientes consejos:

— `### TU CÓDIGO AQUÍ ###` indica dónde debes escribir el código. Asegúrate de reemplazarlo con tu propio código antes de ejecutar la celda de código.
— Siéntete libre de abrir las pistas para obtener información adicional a medida que trabajas en cada tarea.
— Para ingresar tu respuesta a una pregunta, haz doble clic en la celda de markdown para editar. Asegúrate de reemplazar “[Haz doble clic para ingresar aquí tus respuestas.]” con tu propia respuesta.
— Puedes guardar tu trabajo manualmente haciendo clic en Archivo y luego en Guardar en la barra de menú en la parte superior del cuaderno.
— Puedes descargar tu trabajo localmente haciendo un clic en Archivo y luego en Descargar, luego puedes especificar el formato de archivo que prefieras en la barra de menú en la parte superior del cuaderno.
</details>

## Situación hipotética

Trabajas como analista de seguridad. En primer lugar, eres responsable de comprobar si el sistema operativo de un usuario requiere una actualización. A continuación, tienes que investigar los intentos de inicio de sesión en un dispositivo específico. Debes determinar si los intentos de inicio de sesión fueron realizados por usuarios autorizados para acceder a este dispositivo y si dichos intentos se produjeron durante el horario de la organización.

## Tarea 1
Se te pide que ayudes a automatizar el proceso de comprobar si el sistema operativo de un usuario requiere una actualización. Imagina que el dispositivo de un usuario puede ejecutar uno de los siguientes sistemas operativos: OS 1, OS 2 u OS 3. Mientras que OS 2 está actualizado, OS 1 y OS 3 no lo están. Tu tarea consiste en verificar si el sistema del usuario está actualizado y, si lo está, mostrar un mensaje en consecuencia. Para ello, completa la sentencia condicional usando la palabra clave `if`. Asegúrate de reemplazar el fragmento `### TU CÓDIGO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda. 


```python
# Asigna una variable llamada `system` a un sistema operativo específico, representado como una cadena
# Esta variable indica qué sistema operativo se está ejecutando

system = "OS 2"

# Si se está ejecutando OS 2, muestra un mensaje de "no es necesario actualizar"

if system == "OS 2":
    print(“no es necesario actualizar”)
    
```

    no es necesario actualizar


<details>
    <summary><h4><strong>Pista 1</strong></h4></summary>

Utiliza un operador de comparación que te permitirá verificar si el `system` está ejecutando `"OS 2"`.
    
</details>

<details>
    <summary><h4><strong>Pista 2</strong></h4></summary>

Utiliza el operador de comparación `==` para verificar si el `system` está ejecutando `"OS 2"`.
    
</details>

## Tarea 2
Ahora prueba a asignar la variable `system` diferentes valores (`"OS 1"`, `"OS 2"` y `"OS 3"`), ejecuta la celda y observa qué ocurre. Mantén la sentencia condicional como está. Asegúrate de reemplazar el fragmento `### TU CÓDIGO AQUÍ ###` con tu propio código. 


```python
# Asigna a `system` un sistema operativo específico
# Esta variable representa el sistema operativo que se está ejecutando
# No dudes en ejecutar esta celda varias veces; cada vez prueba asignar a `system` diferentes valores ("OS 1", "OS 2", "OS 3") y observa el resultado

system = "OS 1" 

# Si se está ejecutando OS 2, muestra un mensaje de "no es necesario actualizar"

if system == "OS 2":
    print(“no es necesario actualizar”)
    
```

#### **Pregunta 1**
**¿Qué sucede cuando OS 2 se está ejecutando? ¿Qué sucede cuando OS 1 se está ejecutando?**

Cuando se está ejecutando OS 2, se muestra `no es necesario actualizar`. Cuando se está ejecutando OS 1, no se muestra nada. La sentencia `print` anterior solo se ejecuta cuando la condición `system == "OS 2"` se evalúa como `True`.

## Tarea 3

No se muestra nada cuando el `system` no es igual a `"OS 2"`. Esto se debe a que la condición no se evaluó como `True`.

Sería beneficioso si se les proporciona un mensaje alternativo cuando se necesitan realizar actualizaciones.

En la siguiente celda, agrega la palabra clave apropiada después de la primera sentencia condicional para que se muestre un mensaje que transmita que se necesita una actualización cuando el `system` no está ejecutando OS 2. Asegúrate de reemplazar el fragmento `### TU CÓDIGO AQUÍ ###` con tu propio código. 

A continuación, establece el valor de la variable `system` para indicar que OS 2 se está ejecutando y ejecuta la celda. Después de observar lo que sucede, establece el valor de `system` para indicar que OS 1 se está ejecutando o que OS 3 se está ejecutando y ejecuta la celda. 


```python
# Asigna a `system` un sistema operativo específico
# Esta variable representa el sistema operativo que se está ejecutando

system = "OS 3"

# Si se está ejecutando OS 2, muestra un mensaje de "no es necesario actualizar"
# En caso contrario, muestra un mensaje de “es necesario actualizar”

if system == "OS 2":
    print(“no es necesario actualizar”)
else:
    print(“es necesario actualizar”)
    
```

    es necesario actualizar

<details>
    <summary><h4><strong>Pista 1</strong></h4></summary>

Utiliza la palabra clave `else`.
    
</details>

#### **Pregunta 2**
**En esta configuración, ¿qué sucede cuando OS 2 se está ejecutando? ¿Y qué ocurre cuando OS 2 no se está ejecutando? **

En esta configuración, cuando se está ejecutando OS 2, se muestra `no es necesario actualizar`. Y cuando no se está ejecutando OS 2, se muestra `es necesario actualizar`. 

## Tarea 4

Esta configuración sigue sin ser la ideal. Si la variable `system` contiene una cadena aleatoria o un entero, la sentencia condicional anterior seguiría mostrando `es necesario actualizar`.

Para mejorar la sentencia condicional, deberás agregar la palabra clave `elif`. En la siguiente celda, agregarás dos sentencias `elif` después de la sentencia `if`, para crear el código final. La primera sentencia `elif` mostrará `es necesario actualizar` si `system` es `"OS 1"`. La segunda sentencia `elif` mostrará el mismo mensaje, si `system` es `"OS 3"`. Completa la segunda instrucción `elif` y luego ejecuta la celda con la variable `system` ajustada a una cadena diferente cada vez. Observa qué ocurre cuando se ejecuta cada sistema operativo. También prueba a asignar la variable `system` otras cadenas distintas de `"OS 1"`, `"OS 2"` y `"OS 3"` (por ejemplo, `"OS 4"`).

Asegúrate de reemplazar el fragmento `### TU CÓDIGO AQUÍ ###` con tu propio código.


```python
# Asigna a `system` un sistema operativo específico
# Esta variable representa el sistema operativo que se está ejecutando

system = "OS 4"

# Si se está ejecutando OS 2, muestra un mensaje de "no es necesario actualizar"
# En caso contrario, si se está ejecutando OS 1, muestra un mensaje de “es necesario actualizar”
# En caso contrario, si se está ejecutando OS 3, muestra un mensaje de “es necesario actualizar”

if system == "OS 2":
    print(“no es necesario actualizar”)
elif system == "OS 1":
    print(“es necesario actualizar”)
elif system == "OS 3":
    print(“es necesario actualizar”)
    
```

#### **Pregunta 3**
**Con esta configuración, ¿qué sucede cuando OS 2 se está ejecutando? ¿Qué sucede cuando OS 1 se está ejecutando? ¿Qué sucede cuando OS 3 se está ejecutando? ¿Qué sucede cuando ninguno de esos tres sistemas operativos se está ejecutando?**

Con esta configuración, cuando se está ejecutando OS 2, se muestra `no es necesario actualizar`. Cuando se está ejecutando OS 1 o OS 3, se muestra `es necesario actualizar'. Cuando ninguno de los tres sistemas operativos se está ejecutando, no se muestra nada.

## Tarea 5
Escribir código legible y conciso es una de las mejores prácticas en programación.

La sentencia condicional anterior se puede escribir de forma más concisa.

En la siguiente celda, usa un operador lógico para combinar las dos sentencias `elif` de la configuración anterior en una sola sentencia `elif`. Asegúrate de reemplazar cada `### TU CÓDIGO AQUÍ ###`. A continuación, asigna un valor a la variable `system` y ejecuta la celda. Como hiciste en la tarea anterior, usa `"OS 1"`, `"OS 2"`, `"OS 3"` y otras cadenas.


```python
# Asigna a `system` un sistema operativo específico
# Esta variable representa el sistema operativo que se está ejecutando

system = "OS 4"

# Si se está ejecutando OS 2, muestra un mensaje de "no es necesario actualizar"
# En caso contrario, si se está ejecutando OS 1 u OS 3, muestra un mensaje de “es necesario actualizar”

if system == "OS 2":
    print(“no es necesario actualizar”)
elif system == "OS 1" or system == "OS 3": 
    print(“es necesario actualizar”)
    
```

<details>
    <summary><h4><strong>Pista 1</strong></h4></summary>

Utiliza el operador lógico `or`.
    
</details>

<details>
    <summary><h4><strong>Pista 2</strong></h4></summary>

Utiliza el operador `or` entre dos condiciones que utilicen cada una el operador `==`.
    
</details>

#### **Pregunta 4**
**¿Qué observas en esta sentencia condicional?**

Esta sentencia condicional se comporta igual que la anterior. La única diferencia es que la sintaxis de esta sentencia condicional es más concisa. El uso del operador `or` te permite combinar las dos condiciones en una sola sentencia `elif`, que es más concisa que tener las dos sentencias `elif` separadas que se escribieron anteriormente. 

## Tarea 6
Ahora pasarás a la siguiente parte de tu trabajo. Te han pedido que investigues los intentos de inicio de sesión en un dispositivo específico. Solo los usuarios autorizados deben iniciar sesión en este dispositivo.

Comenzarás con dos usuarios autorizados, almacenados en las variables `approved_user1` y `approved_user2`. Deberás escribir una sentencia condicional que compare esas variables con una tercera variable, `username`.  Este será el nombre de usuario de un usuario específico que intenta iniciar sesión. Asegúrate de reemplazar el fragmento `### TU CÓDIGO AQUÍ ###` con tu propio código.


```python
# Asigna `approved_user1` y `approved_user2` a los nombres de usuario de los usuarios autorizados

approved_user1 = "elarson"
approved_user2 = "bmoreno"

# Asigna `username` al nombre de usuario de un usuario específico que intenta iniciar sesión

username = "bmoreno"

# Si el usuario que intenta iniciar sesión se encuentra entre los usuarios autorizados, se mostrará un mensaje indicando que está autorizado para acceder a este dispositivo
# En caso contrario, se mostrará un mensaje indicando que no tiene acceso a este dispositivo

if username == approved_user1 or username == approved_user2:
    print(“Este usuario tiene acceso a este dispositivo.”)
else:
    print(“Este usuario no tiene acceso a este dispositivo.”)
    
```

    Este usuario tiene acceso a este dispositivo.


<details>
    <summary><h4><strong>Pista 1</strong></h4></summary>

Utiliza la palabra clave `if` en la primera sentencia condicional y la palabra clave `else` en la segunda sentencia condicional. Asegúrate de que ambas sentencias terminan con la sintaxis adecuada de dos puntos (`:`).
    
</details>

<details>
    <summary><h4><strong>Pista 2</strong></h4></summary>

Utiliza un operador de comparación que te permita verificar si el usuario que intenta iniciar sesión es un usuario autorizado.
    
</details>

<details>
<summary><h4><strong>Pista 3</strong></h4></summary>

Utiliza el operador de comparación `==` para verificar si el usuario que intenta iniciar sesión es un usuario autorizado.
    
</details>

## Tarea 7
El número de usuarios autorizados se ha ampliado a cinco. En lugar de almacenar cada uno de los nombres de usuario de los usuarios autorizados individualmente, sería más conciso almacenarlos en una lista de permisos llamada `approved_list`.

El operador `in` de Python se puede usar para determinar si un valor dado es un elemento de una secuencia. Usar el operador `in` en una condición puede ayudarte a verificar si un nombre de usuario específico forma parte de una lista de nombres de usuario autorizados. Por ejemplo, en el siguiente código, `username in approved_list` se evalúa como `True` si el valor de la variable `username` está incluido en `approved_list`.

Completa el código en la siguiente celda para mostrar los mismos mensajes que usaste en el paso anterior.  Cuando la condición se evalúa como `True`, se mostrará el siguiente mensaje: “Este usuario tiene acceso a este dispositivo”.Cuando se evalúa como `False`, se mostrará el siguiente mensaje: “Este usuario no tiene acceso a este dispositivo”.A continuación, ejecuta la celda para observar su comportamiento. Asegúrate de reemplazar cada `### TU CÓDIGO AQUÍ ###` con tu propio código. Después, reasigna la variable `username` a un nombre de usuario que no esté autorizado y ejecuta la celda para observar lo que ocurre.


```python
# Asigna `approved_list` a una lista de nombres de usuario autorizados

approved_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]

# Asigna `username` al nombre de usuario de un usuario específico que intenta iniciar sesión

username = "jhill" 

# Si el usuario que intenta iniciar sesión se encuentra entre los usuarios autorizados, se mostrará un mensaje indicando que está autorizado para acceder a este dispositivo
# En caso contrario, se mostrará un mensaje indicando que no tiene acceso a este dispositivo

if username in approved_list:
    print(“Este usuario tiene acceso a este dispositivo.”)
else:
    print(“Este usuario no tiene acceso a este dispositivo.”)
    
```

    Este usuario no tiene acceso a este dispositivo.


<details>
    <summary><h4><strong>Pista 1</strong></h4></summary>

Utiliza la palabra clave `else` en la segunda sentencia condicional.
    
</details>

<details>
    <summary><h4><strong>Pista 2</strong></h4></summary>

Utiliza la función `print()` para mostrar mensajes.
    
</details>

#### **Pregunta 5**
**¿Qué ocurre cuando un usuario autorizado intenta iniciar sesión? ¿Qué ocurre cuando un usuario no autorizado intenta iniciar sesión?**

Cuando un usuario autorizado intenta iniciar sesión, se muestra `"Este usuario tiene acceso a este dispositivo."`. Cuando un usuario no autorizado intenta iniciar sesión, se muestra "`Este usuario no tiene acceso a este dispositivo."`.

## Tarea 8

Ahora escribirás otra sentencia condicional. Esta usará una variable `organization_hours` para verificar si el usuario inició sesión durante horas específicas de la organización. Cuando se cumpla esa condición, el código debe mostrar la cadena `"Intento de inicio de sesión realizado durante el horario de la organización".`. Cuando no se cumpla esa condición, el código debe mostrar la cadena `"Intento de inicio de sesión realizado fuera del horario de la organización".`. 

La variable `organization_hours` tendrá un tipo de dato booleano. Si `organization_hours` tiene un valor booleano `True`, significa que el usuario inició sesión durante el horario de la organización especificado. Si `organization_hours` tiene un valor booleano `False`, significa que el usuario no inició sesión durante ese horario.

Completa la sentencia condicional en la siguiente celda. Asegúrate de reemplazar cada fragmento `### TU CÓDIGO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda.


```python
# Asigna `organization_hours` a un valor booleano que represente si el usuario intenta iniciar sesión durante el horario de la organización

organization_hours = True

# Si el valor de `organization_hours` ingresado es True, se mostrará “Intento de inicio de sesión realizado durante el horario de la organización”.
# En caso contrario, se mostrará "Intento de inicio de sesión realizado fuera del horario de la organización".

if organization_hours == True:
    print("Intento de inicio de sesión realizado durante el horario de la organización.")
else:
    print("Intento de inicio de sesión realizado fuera del horario de la organización.")
    
```

    El intento de inicio de sesión se realizó durante el horario de la organización.


<details>
    <summary><h4><strong>Pista 1</strong></h4></summary>

Utiliza el operador de comparación `==` para comprobar si el usuario ha iniciado sesión durante el horario de la organización especificado. Compara `organization_hours` con el valor booleano apropiado.
    
</details>

<details>
    <summary><h4><strong>Pista 2</strong></h4></summary>

Utiliza la función `print()` para mostrar mensajes.
    
</details>

<details>
<summary><h4><strong>Pista 3</strong></h4></summary>

Utiliza la palabra clave `else` en la segunda sentencia condicional.
    
</details>

#### **Pregunta 6**
**¿Qué sucede cuando el usuario inicia sesión durante el horario de la organización? ¿Qué sucede cuando inicia sesión fuera del horario de la organización?**

Cuando el usuario inicia sesión durante el horario de la organización, la condición de la sentencia `if` se evalúa como `True`, y se muestra un mensaje sobre el intento de inicio de sesión durante el horario de la organización. Cuando el usuario inicia sesión fuera del horario de la organización, la condición de la sentencia `if` se evalúa como `False`. Esto significa que se ejecuta la sentencia `else` y se muestra un mensaje sobre el intento de inicio de sesión fuera del horario de la organización.

## Tarea 9
La siguiente celda ensambla el código de las tareas anteriores. Incluye la sentencia condicional que verifica si un usuario está en la lista de permisos y la sentencia condicional que verifica si el usuario inició sesión durante el horario de la organización.

Ejecuta la celda a continuación varias veces. Cada vez, ingresa una combinación diferente de valores para `username` y `organization_hours` para observar cómo afecta a la salida.


```python
# Asigna `approved_list` a una lista de nombres de usuario autorizados

approved_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]

# Asigna `username` al nombre de usuario de un usuario específico que intenta iniciar sesión

username = "bmoreno"

# Si el usuario que intenta iniciar sesión se encuentra entre los usuarios autorizados, se mostrará un mensaje indicando que está autorizado para acceder a este dispositivo
# En caso contrario, se mostrará un mensaje indicando que no tiene acceso a este dispositivo

if username in approved_list:
    print(“Este usuario tiene acceso a este dispositivo.”)

else:
    print(“Este usuario no tiene acceso a este dispositivo.”)

# Asigna `organization_hours` a un valor booleano que represente si el usuario intenta iniciar sesión durante el horario de la organización

organization_hours = True

# Si el valor de `organization_hours` ingresado es True, se mostrará “Intento de inicio de sesión realizado durante el horario de la organización”.
# En caso contrario, se mostrará "Intento de inicio de sesión realizado fuera del horario de la organización".

if organization_hours == True:
    print("Intento de inicio de sesión realizado durante el horario de la organización.")
else:
    print("Intento de inicio de sesión realizado fuera del horario de la organización.")
    
```

    Este usuario tiene acceso a este dispositivo.
    El intento de inicio de sesión se realizó durante el horario de la organización.


#### **Pregunta 7**
**¿Qué ocurre cuando el usuario que intenta iniciar sesión no se encuentra entre los usuarios autorizados? ¿Qué ocurre cuando el usuario que intenta iniciar sesión se encuentra entre los usuarios autorizados? ¿Qué ocurre cuando el usuario intenta iniciar sesión fuera del horario de la organización?**

Cuando el usuario que intenta iniciar sesión no se encuentra entre los usuarios autorizados, se muestra un mensaje indicando que el usuario no tiene acceso al dispositivo. El código luego verifica si el usuario intentó iniciar sesión durante el horario de la organización.

Cuando el usuario que intenta iniciar sesión se encuentra entre los usuarios autorizados, se muestra un mensaje indicando que el usuario tiene acceso al dispositivo y, a continuación, el código comprueba si ha intentado iniciar sesión durante el horario de la organización. Cuando el usuario que intenta iniciar sesión lo hace fuera del horario de la organización, se muestra un mensaje sobre el intento de inicio de sesión fuera del horario de la organización.

## Tarea 10
También puedes proporcionar un único mensaje sobre el intento de inicio de sesión. Para ello, puedes unir ambas condiciones en una sola sentencia condicional utilizando un operador lógico. Esto hará que el código sea más conciso.

Examina el código de la siguiente celda y agrega el operador que falta para que aparezca un único mensaje. Asegúrate de reemplazar cada `### TU CÓDIGO AQUÍ ###` con tu propio código antes de ejecutar la siguiente celda. A continuación, ejecuta la celda, ingresando diferentes combinaciones de información y observa lo que ocurre.


```python
# Asigna `approved_list` a una lista de nombres de usuario autorizados

approved_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]

# Asigna `username` al nombre de usuario de un usuario específico que intenta iniciar sesión

username = "bmoreno"

# Asigna `organization_hours` a un valor booleano que represente si el usuario intenta iniciar sesión durante el horario de la organización

organization_hours = True

# Si el usuario se encuentra entre los usuarios autorizados y está iniciando sesión durante el horario de la organización, comunica que el usuario ha iniciado sesión
# En caso contrario, comunica que el nombre de usuario no está autorizado o que el intento de inicio de sesión se realizó fuera del horario de la organización
 
if username in approved_list and organization_hours == True:
    print("Intento de inicio de sesión realizado por un usuario autorizado durante el horario de la organización.")
else:
    print("Nombre de usuario no autorizado o intento de inicio de sesión realizado fuera del horario de la organización.")
    
```

    Intento de inicio de sesión realizado por un usuario autorizado durante el horario de la organización.


<details>
    <summary><h4><strong>Pista 1</strong></h4></summary>

Utiliza el operador lógico que te permita verificar ambas condiciones en la sentencia `if` (la condición de que el nombre de usuario ingresado está en la lista de autorizados y la condición de que el intento de inicio de sesión ocurre durante el horario de la organización).
    
</details>

<details>
    <summary><h4><strong>Pista 2</strong></h4></summary>

Utiliza el operador lógico `and` para verificar las dos condiciones de la sentencia `if` (la condición de que el nombre de usuario ingresado está en la lista de autorizados y la condición de que el intento de inicio de sesión ocurre durante el horario de la organización).
    
</details>

#### **Pregunta 8**
**En esta configuración, ¿qué ocurre cuando el usuario que intenta iniciar sesión es un usuario autorizado y lo hace durante el horario de la organización? ¿Qué sucede cuando el usuario no está autorizado o intenta iniciar sesión fuera del horario de la organización?**

En esta configuración, cuando el usuario está autorizado e intenta iniciar sesión durante el horario de la organización, se muestra el mensaje `"Intento de inicio de sesión realizado por un usuario autorizado durante el horario de la organización."`. Si el usuario no está autorizado o intenta iniciar sesión fuera del horario de la organización, se mostrará el mensaje `"Nombre de usuario no autorizado o intento de inicio de sesión realizado fuera del horario de la organización."`. Este código comprueba las mismas condiciones que el código de la tarea anterior. Sin embargo, las une en una sentencia `if`, y tanto `username` como `organization_hours` se investigan antes de que se muestre un solo mensaje.

## Conclusión
**¿Qué conclusiones clave obtuviste de este laboratorio?**
*   Las sentencias condicionales, los operadores de comparación y los operadores lógicos desempeñan un papel importante en la automatización de procesos importantes para mantener la seguridad, como detectar cuándo el sistema operativo de un usuario requiere actualizaciones y detectar cuándo se permite a un usuario acceder a un dispositivo. 
*   Las sentencias condicionales te permiten determinar si se cumple un conjunto específico de condiciones. 
* Los operadores de comparación te permiten comparar pares de valores. En concreto, el operador `==` te permite determinar si un valor es igual a otro.
*   Los operadores lógicos como `and` y `or` te permiten verificar más de una condición a la vez.




