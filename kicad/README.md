## **Introducción a KiCad**

KiCad es un software de diseño de circuitos electrónicos de código abierto, 
utilizado para la creación de esquemas eléctricos y diseño de placas de circuito 
impreso (PCB). Es una herramienta ampliamente utilizada tanto por aficionados 
como por profesionales debido a su versatilidad y capacidad para manejar 
proyectos complejos.

### Características principales:
- Editor de esquemáticos avanzado con bibliotecas de componentes personalizables.
- Generación y gestión de archivos Gerber para la fabricación de PCBs.
- Integración con simuladores de circuitos.
- Vista 3D del diseño de la PCB para visualización realista.

---


### Instalación e Interfaz

Para comenzar a trabajar con KiCad, es importante conocer cómo se configura la 
interfaz y algunos aspectos básicos antes de diseñar esquemáticos y PCBs.

## Configuración de la Página  

Antes de empezar un proyecto, KiCad permite configurar los parámetros del 
diseño, como la información del título y el tamaño de la hoja.

### Pasos para configurar la página:  
1. Ir a **`File > Page Settings`**.  
2. Configurar los siguientes campos según tus necesidades:  
   - **Issue Date** (Fecha de emisión)  
   - **Revisión**  
   - **Título del proyecto**  
   - **Compañía**  
   - **Comentarios adicionales**  
3. Seleccionar el **tamaño de la hoja** (Ejemplo: A4).  

**Sugerencia:** Personaliza estos parámetros desde el inicio si trabajas en un 
entorno profesional o necesitas un formato estandarizado. Sin embargo, si estás 
en fase de prototipado o pruebas, puedes configurarlos más adelante sin 
problema.


---


### Atajos de Teclado en KiCad

Para agilizar el flujo de trabajo en KiCad, es recomendable aprender algunos 
atajos de teclado. Esto permite realizar acciones más rápidamente sin depender 
del uso del mouse.

#### Cómo acceder a la lista de atajos:  
- Ir a **`Help > List Hotkeys`**.

A continuación, algunos de los atajos más utilizados:

---

### Atajos en el editor de esquemáticos  
Estos comandos se usan mientras se diseña el esquema eléctrico:  

| Acción                           | Tecla  |
|----------------------------------|--------|
| Agregar un símbolo              | **A**  |
| Agregar fuente de poder         | **P**  |
| Reflejar un componente en X     | **X**  |
| Reflejar un componente en Y     | **Y**  |
| Mover un componente             | **M**  |
| Iniciar un cableado             | **W**  |
| Agregar etiqueta a una señal    | **L**  |
| Editar el footprint de un símbolo | **F**  |
| Editar referencia del símbolo   | **U**  |
| Editar propiedades de un elemento | **E**  |
| Copiar un elemento              | **C**  |

*Sugerencia:* Usar **X/Y** para reflejar componentes y **M** para moverlos sin 
necesidad de seleccionar la herramienta en la barra de herramientas.

---

### Atajos en el editor de PCB
Estos comandos se utilizan cuando se trabaja en el diseño de la PCB:

| Acción                         | Tecla  |
|--------------------------------|--------|
| Mover un componente           | **M**  |
| Rotar un componente           | **R**  |
| Iniciar una nueva pista       | **X**  |
| Insertar una vía              | **V**  |
| Rellenar las zonas de cobre   | **B**  |
| Borrar un elemento            | **Delete** |

*Sugerencia:* Usar **B** periódicamente en el editor de PCB rellena las zonas de cobre, 
permitiendo visualizar mejor la distribución de las conexiones.

---

### Conclusión
Aprender estos atajos reducirá el tiempo empleado en tareas repetitivas y hará 
que el proceso de diseño sea más eficiente.


---


### Diseño de Esquemático  

El diseño esquemático es la primera etapa en la creación de un circuito impreso 
en KiCad. En esta fase, se agregan y conectan los componentes electrónicos de 
manera lógica antes de trasladarlos al diseño físico de la PCB.

---

## Creación de un Proyecto  

Para iniciar un nuevo proyecto en KiCad, sigue estos pasos:

1. Ir a **`File > New Project`**.  
2. Crear una carpeta y asignarle un nombre significativo al proyecto.  
3. Abrir el archivo esquemático haciendo doble clic sobre él en la lista de 
   archivos del proyecto.  

*Sugerencia:* Mantener los archivos organizados en una carpeta facilita la gestión 
del proyecto y evita problemas con la ubicación de bibliotecas y archivos 
asociados.

---

## Creación de Símbolos Personalizados  

Si un componente no está disponible en la biblioteca de KiCad, es posible crearlo 
manualmente en el **Editor de Símbolos**.

### Pasos para crear un símbolo nuevo:  
1. Abrir **`Symbol Editor`**.  
2. Crear una nueva biblioteca en **`File > New Library`** y guardarla como global 
   para su uso en futuros proyectos.  
3. Presionar **`New Symbol`** y definir:  
   - **Nombre del símbolo** (Ejemplo: `FT232RL`).  
4. Dibujar el símbolo:  
   - Agregar un rectángulo (**Add Rectangle**) para representar el cuerpo del componente.  
   - Insertar pines con **`Add Pin`** o la tecla **P**.  
   - Configurar los pines con:  
     - **Nombre** (Ejemplo: `TXD`).  
     - **Número de pin** (Ejemplo: `1`).  
     - **Tipo de pin** (`Input`, `Output`, `Power`, etc.).  
5. Guardar el símbolo en la nueva biblioteca.  

*Sugerencia:* Verificar el **datasheet** del componente para asegurarse de que la 
cantidad de pines, nombres y tipos sean correctos antes de guardar el símbolo.

---

### Inserción de Componentes en el Esquemático  
1. Presionar **A** o seleccionar **`Add Symbol`**.  
2. Buscar el componente por su nombre (Ejemplo: `LM1117`).  
3. Insertar componentes comunes como:  
   - Resistencias (**`R`**).  
   - Condensadores (**`C`**).  
4. Rotar los componentes con la tecla **R** si es necesario.  

---

### Conexiones Eléctricas  
- Conectar los pines con **`Add Wire`** (tecla **W**).  
- Para evitar cables largos y desordenados, utilizar etiquetas con **`Add Label`** (tecla **L**).  
- Modificar valores de componentes presionando **E** sobre ellos.  
- Marcar pines no conectados con **`Add Not Connect Flag`**.

---

### Anotación del Esquema  
Para asignar identificadores a los componentes del circuito:  
1. Presionar **`Annotate Schematic`**.  
2. O ir a **`Tools > Annotate Schematic`**.  
3. Confirmar los cambios y revisar la numeración de los componentes.  

---

### Verificación de Errores Eléctricos  
Antes de avanzar al diseño de PCB, se recomienda comprobar la validez del 
esquema eléctrico:  
1. Abrir **`Electrical Rules Checker`**.  
2. O ir a **`Inspect > Electrical Rules Checker`**.  
3. Revisar advertencias y corregir errores.  

*Sugerencia:* Un error común es la conexión incorrecta de pines con diferentes tipos 
eléctricos (Ejemplo: `Power Input` con `Passive`). Si esto ocurre, se puede editar 
el símbolo o reemplazarlo por uno con la configuración correcta.


---


