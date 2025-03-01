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

- **Acceso al Editor de Símbolos:**
  - Dirígete a `Tools` > `Symbol Editor` desde el menú principal de KiCad.

- **Creación de una Nueva Biblioteca:**
  - Es recomendable crear una biblioteca personalizada para almacenar tus 
  símbolos. Esto se logra seleccionando `File` > `New Library` y definiendo su 
  ubicación.

  - Si trabajas en varios proyectos y quieres reutilizar los componentes en el 
  futuro, mantener la biblioteca como **global** es más eficiente.
  - Si necesitas compartir el proyecto o asegurarte de que siempre tenga los 
  componentes personalizados disponibles, entonces incluir la biblioteca dentro 
  del **proyecto** es lo mejor.

  - Se le asigna un nombre a la Library. 

- **Definición del Símbolo:**
  - Al crear un nuevo símbolo (`File` > `New Symbol`), establece el nombre y 
  asócialo a la biblioteca creada.

  - Aosciar el Simbolo a la biblioteca:
    - Seleccionar la biblioteca correcta:
      En la parte izquierda, busca la biblioteca <nombre_lib>.kicad_sym.
      Si no aparece, agrégala manualmente en:
      Preferences > Manage Symbol Libraries > Project Specific Libraries > 
      Add Library.
      Selecciona <nombre_lib>.kicad_sym y asegúrate de que esté activa.
      Luego Save all.

  - Asegúrate de que el origen (0,0) esté bien definido para facilitar la 
  colocación del símbolo en los esquemas.

- **Configuración de la Cuadrícula:**
  - Ajusta la cuadrícula a un valor adecuado (por ejemplo, 50 mils) para 
  garantizar una alineación precisa de los pines.

- **Adición de Pines:**
  - Utiliza la herramienta de agregar pines para incorporar cada pin necesario, 
  asignando nombres, números y configurando la orientación y tipo de cada uno 
  (entrada, salida, bidireccional, etc.).

- **Dibujo del Cuerpo del Símbolo:**
  - Emplea las herramientas de dibujo para crear la representación gráfica del 
  componente, asegurando que los pines estén correctamente posicionados.

- **Guardado y Verificación:**
  - Guarda el símbolo y verifica su correcta integración insertándolo en un 
  esquema de prueba.

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



### **2. Creación de Footprints Personalizados**

- **Acceso al Editor de Footprints:**
  - Desde el menú principal de KiCad, selecciona `Herramientas` > `Editor de huellas`.

- **Creación de una Nueva Biblioteca de Footprints:**
  - Al igual que con los símbolos, es aconsejable crear una biblioteca específica para tus footprints personalizados.

- **Definición del Footprint:**
  - Crea un nuevo footprint (`Archivo` > `Nueva huella`) y asígnale un nombre representativo.

- **Configuración de la Cuadrícula:**
  - Ajusta la cuadrícula según el paso de los pines del componente (por ejemplo, 0.5 mm) para una colocación precisa.

- **Adición de Pads:**
  - Utiliza la herramienta de agregar pads para colocar las áreas de contacto, configurando su forma, tamaño y asignando los números de pin correspondientes.

- **Dibujo del Contorno del Componente:**
  - Emplea las capas gráficas adecuadas para delinear el contorno físico del componente, facilitando su correcta colocación durante el ensamblaje.

- **Definición del Punto de Origen:**
  - Establece el origen en el pad correspondiente al pin 1 o en una posición central, según convenga para el diseño.

- **Asociación con el Símbolo:**
  - En el Editor de Esquemáticos, asigna el footprint creado al símbolo correspondiente mediante las propiedades del componente.

- **Guardado y Verificación:**
  - Guarda el footprint y verifica su correcta implementación colocándolo en un diseño de PCB de prueba.

### **3. Recursos Adicionales**

Para profundizar en estos procesos, te recomiendo los siguientes recursos:

- **Documentación Oficial de KiCad:**
  - Proporciona guías detalladas sobre la creación y gestión de símbolos y footprints.

- **Tutorial en Video:**
  - El siguiente video ofrece una demostración práctica de la creación de símbolos y footprints en KiCad:

videoCreación de SÍMBOLO Y HUELLA en KiCad - IngeDonManualturn0search0

Incorporando estos detalles a tus notas, podrás ofrecer una guía más completa y práctica para la creación de símbolos y footprints en KiCad. 