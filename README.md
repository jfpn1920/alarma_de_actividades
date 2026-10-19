<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:007ACC,100:5DADE2&height=260&section=header&text=Alarma%20de%20actividades&desc=Bienvenidos%20usuarios%20a%20mi%20proyecto&fontSize=43&fontColor=ffffff&descSize=18&fontAlignY=38&descAlignY=58&animation=fadeIn"/>

<p align="justify">Este proyecto, llamado <b>alarma de actividades</b>, fue desarrollado en <b>pseint</b> como un ejercicio práctico para fortalecer la lógica de programación mediante la creación de un sistema de gestión de actividades desde la consola. El programa cuenta con un menú principal de siete opciones que permite <b>registrar, editar, eliminar, buscar, listar y consultar los detalles</b> de las actividades registradas. Cada actividad almacena datos como el identificador, el título, la fecha, la hora, el lugar, la prioridad, la descripción y el estado, utilizando arreglos con una capacidad de <b>100 posiciones durante la ejecución</b>. Durante su desarrollo se aplicaron conceptos fundamentales de programación, como variables, arreglos, estructuras condicionales, ciclos repetitivos y estructuras de selección, además de procesos para buscar, modificar, eliminar y reorganizar registros. Este proyecto permite poner en práctica los conocimientos adquiridos en PSeInt y sirve como base para desarrollar sistemas de gestión más avanzados utilizando otros lenguajes y tecnologías.</p>

<h2 align="center">⚙️ Funcionamiento del menú principal</h2>

### ➕ Registrar actividad

<p align="justify">La opción <b>1) registrar actividad</b> permite añadir una nueva actividad a la alarma. El programa asigna automáticamente un <b>id</b> mediante la variable <b>siguienteID</b>, que aumenta en uno con cada registro, y lo muestra en pantalla. Después, solicita el <b>título, la fecha, la hora, el lugar, la prioridad, la descripción y el estado</b>, y guarda cada dato en la posición correspondiente de sus arreglos (<b>totalActividades + 1</b>). Finalmente, la variable <b>totalActividades</b> aumenta en uno y se muestra el mensaje <b>"actividad registrada correctamente."</b>.</p>

### ✏️ Editar actividad

<p align="justify">La opción <b>2) editar actividad</b> permite modificar la información de una actividad registrada. Primero, el programa comprueba si <b>totalActividades</b> es igual a cero; si no hay registros, muestra el mensaje <b>"no hay actividades registradas."</b>. En caso contrario, presenta una lista con el id, título, fecha, hora, lugar, prioridad, descripción y estado de cada actividad, y solicita el <b>id</b> de la actividad que se desea editar. Después, inicializa la variable lógica <b>encontrado</b> con el valor <b>falso</b> y utiliza un ciclo <b>para</b> que recorre el arreglo <b>id</b>. Cuando encuentra una coincidencia, cambia <b>encontrado</b> a <b>verdadero</b>, solicita el nuevo <b>título, fecha, hora, lugar, prioridad, descripción y estado</b>, actualiza directamente los valores de los arreglos y muestra el mensaje <b>"alarma de actividad editada correctamente."</b>. Si no existe una actividad con ese id, presenta el mensaje <b>"no se encontró una actividad con ese id."</b>.</p>

### 🗑️ Eliminar actividad

<p align="justify">La opción <b>3) eliminar actividad</b> permite eliminar una actividad registrada mediante su <b>id</b>. Antes de comenzar, el programa comprueba que existan actividades; si no hay, muestra el mensaje <b>"no hay actividades registradas."</b>. Si hay registros, presenta una lista con el id, título, fecha, hora, lugar, prioridad, descripción y estado, y solicita el id de la actividad que se desea eliminar. Un ciclo <b>para</b> recorre el arreglo <b>id</b> en busca de la coincidencia. Cuando la encuentra, cambia <b>encontrado</b> a <b>verdadero</b> y, si la actividad no es la última, utiliza un segundo ciclo <b>para</b> controlado por la variable <b>j</b>, que desplaza una posición hacia atrás los datos de las actividades posteriores en los ocho arreglos. Posteriormente, disminuye la variable <b>totalActividades</b> en uno y muestra el mensaje <b>"alarma de actividad eliminada correctamente."</b>. Si no existe una actividad con ese id, presenta el mensaje <b>"no se encontró una actividad con ese id."</b>.</p>

### 🔎 Buscar actividad

<p align="justify">La opción <b>4) buscar actividad</b> permite localizar una actividad mediante su <b>id</b>. Primero, el programa comprueba si existen actividades registradas. Si no hay, muestra el mensaje <b>"no hay actividades registradas."</b>. En caso contrario, inicializa la variable lógica <b>encontrado</b> con el valor <b>falso</b> y solicita el id. Un ciclo <b>para</b> recorre el arreglo <b>id</b> y compara cada valor con <b>idBuscar</b>. Cuando encuentra una coincidencia, cambia <b>encontrado</b> a <b>verdadero</b> y muestra en una sola línea el id, título, fecha, hora, lugar, prioridad, descripción y estado. Si termina el recorrido sin coincidencias, presenta el mensaje <b>"no se encontró una actividad con ese id."</b>.</p>

### 📋 Listar actividades

<p align="justify">La opción <b>5) listar actividades</b> permite visualizar todas las actividades registradas. Si <b>totalActividades</b> es igual a cero, muestra el mensaje <b>"no hay actividades registradas."</b>. En caso contrario, utiliza un ciclo <b>para</b> que recorre los arreglos desde la primera posición hasta el total de actividades y muestra, en una línea por registro, el <b>id, título, fecha, hora, lugar, prioridad y estado</b>. Esta función facilita consultar las actividades existentes sin necesidad de buscar cada una individualmente.</p>

### 📄 Ver detalles de la actividad

<p align="justify">La opción <b>6) ver detalles de la actividad</b> permite consultar todos los datos de una actividad específica. Primero, comprueba si existen actividades registradas; si no hay, muestra el mensaje <b>"no hay actividades registradas."</b>. Después, solicita el <b>id</b> y recorre el arreglo <b>id</b> en busca de una coincidencia. Si la encuentra, muestra cada dato en su propia línea: <b>id, título, fecha, hora, lugar, prioridad, descripción y estado</b>. Si no existe una actividad con ese id, presenta el mensaje <b>"no se encontró una actividad con ese id."</b>.</p>

### 🚪 Salir del menú principal

<p align="justify">La opción <b>7) salir</b> finaliza la ejecución del programa y muestra el mensaje <b>"gracias por utilizar la alarma de actividades."</b>. El menú principal se encuentra dentro de una estructura repetitiva <b>repetir ... hasta que</b>, cuya condición de salida es <b>opcion = 7</b>, por lo que el menú se mantiene activo hasta que el usuario selecciona la opción de salida.</p>

<h2 align="center">🧠 Temas aplicados en el proyecto</h2>

### 📦 Variables

<p align="justify">En este proyecto se utilizan variables para guardar la opción seleccionada en el menú, controlar la cantidad de actividades registradas, generar los identificadores, recorrer los arreglos, almacenar el id que se desea buscar y comprobar si se encontró una coincidencia. Cada variable cumple una función específica dentro de las operaciones de gestión de actividades.</p>

🔢 **Opcion:** Almacena la opción seleccionada por el usuario en el menú principal.

📊 **TotalActividades:** Almacena la cantidad actual de actividades registradas.

🆔 **SiguienteID:** Almacena el próximo identificador que se asignará a una nueva actividad.

🔄 **I:** Funciona como contador en los ciclos <b>para</b> que recorren los arreglos.

🔁 **J:** Controla el recorrido utilizado para desplazar los datos durante la eliminación de una actividad.

🔎 **IdBuscar:** Almacena el id introducido por el usuario para buscar, editar, eliminar o consultar una actividad.

✅ **Encontrado:** Variable lógica que indica si se encontró una actividad con el id solicitado.

### 🗃️ Arreglos

<p align="justify">En este proyecto se utilizan ocho arreglos relacionados con los datos de cada actividad. Cada arreglo tiene una capacidad de <b>100 posiciones</b> y utiliza el mismo índice para representar la información correspondiente a una misma actividad. Por ejemplo, los datos de una actividad almacenada en la posición <b>1</b> se encuentran distribuidos entre <b>id[1], titulo[1], fecha[1], hora[1], lugar[1], prioridad[1], descripcion[1] y estado[1]</b>. Esta organización permite recorrer, buscar, modificar, mostrar y eliminar las actividades de manera ordenada.</p>

🆔 **Id[100]:** Almacena el identificador único de cada actividad.

📝 **Titulo[100]:** Almacena el título de la actividad.

📅 **Fecha[100]:** Almacena la fecha de la actividad.

⏰ **Hora[100]:** Almacena la hora de la actividad.

📍 **Lugar[100]:** Almacena el lugar donde se realizará la actividad.

🚦 **Prioridad[100]:** Almacena la prioridad de la actividad.

🗒️ **Descripcion[100]:** Almacena una descripción de la actividad.

📌 **Estado[100]:** Almacena el estado de la actividad.

### 🔀 Estructuras condicionales

<p align="justify">En este proyecto se utilizan las estructuras <b>si</b> y <b>sino</b> para comprobar si existen actividades registradas antes de editar, eliminar, buscar, listar o consultar detalles, para identificar la actividad que coincide con el id introducido, para decidir si es necesario desplazar registros al eliminar y para determinar si se encontró el id buscado. Estas condiciones permiten que el programa responda de manera diferente según el estado de los registros y el resultado de cada operación.</p>

### 🔄 Estructuras repetitivas

<p align="justify">En este proyecto se utilizan los ciclos <b>para</b> y <b>repetir ... hasta que</b>. Los ciclos <b>para</b> permiten recorrer los arreglos para mostrar las actividades, buscar ids y acceder a los registros seleccionados. Durante la eliminación, también se utilizan para desplazar los datos de las actividades posteriores una posición hacia atrás. Por otro lado, el ciclo <b>repetir ... hasta que</b> mantiene activo el menú principal para que el usuario pueda ejecutar diferentes operaciones antes de salir del programa.</p>

### 🎯 Estructura según

<p align="justify">El programa evalúa el valor almacenado en la variable <b>opcion</b> y ejecuta el bloque de instrucciones correspondiente. Cada caso representa una operación específica del sistema: <b>registrar, editar, eliminar, buscar, listar, ver detalles o salir</b>. También se utiliza el bloque <b>de otro modo</b> para mostrar el mensaje <b>"opción no válida."</b> cuando el valor introducido no coincide con ninguna de las opciones definidas.</p>

### 🔢 Dimensionamiento de arreglos

<p align="justify">El programa utiliza la instrucción <b>dimension</b> para establecer la capacidad de los arreglos que almacenan la información de las actividades. Se definieron <b>100 posiciones</b> para cada arreglo. La cantidad de posiciones ocupadas se controla mediante la variable <b>totalActividades</b>, por lo que las operaciones recorren únicamente los registros comprendidos entre la primera posición y el total actual de actividades.</p>

### 🆔 Generación automática de identificadores

<p align="justify">Cada vez que se registra una actividad, el programa asigna el valor actual de <b>siguienteID</b> al arreglo <b>id</b> y luego lo aumenta en uno. De esta manera, cada actividad tiene un identificador único que se utiliza para buscarla, editarla, eliminarla y consultar sus detalles, incluso después de eliminar otros registros.</p>

### 🔄 Reorganización de registros

<p align="justify">Cuando se selecciona una actividad para eliminarla y esta no es el último registro, el programa utiliza un ciclo <b>para</b> que comienza en la posición de la actividad y llega hasta <b>totalActividades - 1</b>. En cada repetición, los datos de la posición siguiente se copian sobre la posición actual en los ocho arreglos: <b>id, titulo, fecha, hora, lugar, prioridad, descripcion y estado</b>. Después, la variable <b>totalActividades</b> disminuye en uno. De esta manera, las actividades posteriores ocupan las posiciones disponibles sin dejar espacios vacíos entre los registros activos.</p>

<h2 align="center">¿Cómo se implementaron las operaciones crud en el proyecto?</h2>

<p align="justify">Las operaciones <b>crud</b> se implementaron mediante las opciones del menú principal, permitiendo administrar las actividades registradas. La operación <b>crear</b> corresponde a <b>registrar actividad</b>, donde se introducen los datos de una nueva actividad; <b>leer</b> se realiza mediante las opciones <b>buscar actividad, listar actividades y ver detalles de la actividad</b>; <b>actualizar</b> corresponde a <b>editar actividad</b>, donde se modifican los datos de una actividad registrada; y <b>eliminar</b> se realiza mediante la opción <b>eliminar actividad</b>. Estas operaciones utilizan variables, arreglos, condicionales y ciclos para gestionar la información almacenada temporalmente durante la ejecución del programa.</p>

<h2 align="center">Diagrama de flujo del proyecto</h2>

<img src="./alarma_de_actividades.png" alt="diagrama de flujo de alarma de actividades" width="100%">

<h2 align="center">🛡️ Validaciones del programa</h2>

### 📭 No existen actividades registradas

<p align="justify">Esta validación se utiliza en las opciones de <b>editar, eliminar, buscar, listar y ver detalles</b>. El programa comprueba si la variable <b>totalActividades</b> es igual a <b>0</b> y, si no existen actividades registradas, muestra el mensaje <b>"no hay actividades registradas."</b>. Esta comprobación evita continuar con operaciones que necesitan información almacenada cuando no hay registros.</p>

### ❌ Actividad no encontrada

<p align="justify">Esta validación se utiliza en las opciones de <b>editar, eliminar, buscar y ver detalles</b>. El programa inicializa la variable lógica <b>encontrado</b> con el valor <b>falso</b> y recorre el arreglo <b>id</b> para comparar cada valor con el id introducido. Cuando encuentra una coincidencia, cambia la variable a <b>verdadero</b> y realiza la operación correspondiente. Si al finalizar el recorrido <b>encontrado</b> continúa siendo <b>falso</b>, muestra el mensaje <b>"no se encontró una actividad con ese id."</b>.</p>

### ⚠️ Opción no válida

<p align="justify">La estructura <b>segun</b> incluye el bloque <b>de otro modo</b>, que muestra el mensaje <b>"opción no válida."</b> cuando el usuario introduce un número que no corresponde a ninguna de las opciones definidas en el menú.</p>

<h2 align="center">🚧 Mejoras pendientes</h2>

<p align="justify">Como parte de la evolución del proyecto, se identificaron las siguientes mejoras para versiones futuras:</p>

- ⏰ Agregar una opción que compare la fecha y la hora de las actividades con las actuales, para mostrar recordatorios de las actividades pendientes.
- ⚠️ Validar que <b>totalActividades</b> no supere la capacidad de <b>100</b> posiciones antes de registrar una nueva actividad.
- 🚦 Definir la prioridad como opciones fijas (por ejemplo, alta, media y baja) y validar el formato de la fecha y la hora.
- 🧹 Limpiar la última posición ocupada después de eliminar una actividad.
- 📊 Agregar un listado de actividades filtrado por prioridad o por estado.

<h2 align="center">🎯 Objetivo del proyecto</h2>

<p align="justify">El objetivo principal de este proyecto es fortalecer la <b>lógica de programación</b> mediante el desarrollo de un sistema de gestión de actividades en <b>pseint</b>. A través de su construcción se busca aplicar los conocimientos adquiridos sobre variables, arreglos, estructuras condicionales, ciclos repetitivos y estructuras de selección, integrándolos para resolver un problema de manera organizada. Además, el proyecto permite comprender cómo registrar, consultar, modificar y eliminar información en una aplicación de consola, estableciendo una base para desarrollar sistemas de gestión más completos con otros lenguajes y tecnologías.</p>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:007ACC,100:5DADE2&height=110&section=footer&text=%C2%A9%202026%20%7C%20L%C3%B3gica%20de%20programaci%C3%B3n%20hecha%20en%20pseint%20%7C%20alarma%20de%20actividades&fontSize=14&fontColor=FFFFFF&fontAlignY=87.5"/>