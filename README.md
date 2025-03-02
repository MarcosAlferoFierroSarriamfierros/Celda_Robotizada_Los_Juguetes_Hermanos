# Celda Robotizada y Gestión de Producción: Los Juguetes Hermanos

# Los Juguetes Hermanos: Automatización de Extracción de Piezas e Intercambio de Moldes

**Autor:** Marcos Alfredo Fierro Sarria  
**Curso:** Automatización de Procesos de Manufactura  
**Universidad Nacional de Colombia**  
**Fecha:** 27 de noviembre de 2024

## Índice
1. [Introducción](#introducción)
2. [Objetivo](#objetivo)
3. [Etapas Principales](#etapas-principales)
   - [Identificación y Selección de la Etapa del Proceso](#identificación-y-selección-de-la-etapa-del-proceso)
   - [Selección de Componentes de la Celda](#selección-de-componentes-de-la-celda)
4. [Celda Robotizada: IRB 6700](#celda-robotizada-irb-6700)
   - [LayOut de la Celda](#layout-de-la-celda)
   - [Componentes](#componentes)
   - [Duty Cycle y Throughput time](#duty-cycle-y-throughput-time)
5. [Identificación de Peligros y Gestión de Riesgos](#identificación-de-peligros-y-gestión-de-riesgos)
   - [Riesgos presentes](#riesgos-presentes)
   - [Frecuencia y probabilidad de los peligros](#frecuencia-y-probabilidad-de-los-peligros)
   - [Escalas de Probabilidad y Severidad](#escalas-de-probabilidad-y-severidad)
   - [Clasificación del Nivel de Riesgo](#clasificación-del-nivel-de-riesgo)
   - [Mitigación de los peligros](#mitigación-de-los-peligros)
6. [Referencias](#referencias)

---

## Introducción
En el marco de un proceso de mejora continua y optimización de la producción, la empresa Los Juguetes Hermanos ha identificado oportunidades estratégicas para incrementar la eficiencia en su cadena de manufactura. Con este objetivo, el departamento de ingeniería ha desarrollado un plan integral que contempla la integración de celdas robotizadas, la adquisición de maquinaria avanzada y una redistribución del layout de planta. Estas medidas buscan reducir tiempos de ciclo, minimizar desperdicios y mejorar la flexibilidad operativa.
Actualmente, el proceso central de la producción es la inyección de piezas plásticas, la cual se lleva a cabo mediante tres inyectoras operando simultáneamente. No obstante, el análisis de producción mediante la herramienta de Tecnomatix evidenció un uso ineficiente de los recursos, ya que cada inyectora funcionaba a solo un 66,66\% de su capacidad, dedicándose exclusivamente a la fabricación de un único tipo de producto en cada ciclo de producción. Este esquema generaba tiempos muertos elevados y una subutilización del equipo, impactando negativamente en la productividad y en los costos operativos.
Para abordar esta problemática, se ha propuesto la consolidación de dos celdas robotizadas para operar cada una, una inyectora, optimizada mediante la implementación de un manipulador robótico. Este robot tendrá la función de extraer las piezas inyectadas y realizar el cambio automatizado de moldes, eliminando la necesidad de intervención manual en esta etapa crítica. Con esta solución, el tiempo de configuración (set-up) para el cambio de moldes, que suele encontrarse en el orden de 2 a 3 horas por cada modificación dependiendo del proceso, podrá reducirse a un minuto o menos, lo que representa una disminución superior al 90\% en los tiempos de ajuste. Finalmente, además de la consolidación de celdas robotizadas en la etapa de inyección, el plan de optimización contempla la automatización parcial de los procesos de desbarbado y empaque, dos operaciones clave en la línea de producción.


---

## Objetivo

Detallar las etapas del proceso de fabricación y seleccionar una o varias donde se aplique la implementación de la celda robotizada.Detallar las rutinas del manipulador robótico y componentes necesarios.

---

## Etapas Principales

### Identificación y Selección de la Etapa del Proceso
La fábrica de **Los Juguetes Hermanos** cuenta con las siguientes etapas de producción:

Para realizar el diseño de las celdas automatizadas y el desarrollo de los entregables solicitados, se sigue el diagrama de flujo correspondiente a la figura:

![image](https://github.com/user-attachments/assets/b2748e9a-ec5b-4563-ab4d-ed934434c6c6)


- **Registro:** Es una estación en la que se lleva el inventario de la materia prima que ingresa en la fábrica. Se comprueba peso para verificar la cantidad de pellets que entra en el proceso, otros insumos como la pintura son marcados con códigos de barras.
- **Inyección:** Proceso primario de la fábrica. Es donde se da forma a las piezas que dan vida a nuestros productos. Se usa inyección por presión, lo que permite que el proceso sea productivo.
- **Lijado:** En esta etapa se lija el material proveniente del proceso de inyección, esto se hace para mejorar la adherencia de la pintura en el etapa de pinturado.
- **Desbarbado:**Se remueven excedentes de material producto del proceso de inyección.
- **Pintado:**Se aplica pintura con aerosol de forma manual  sobre las piezas que así lo requieran.
- **Secado:** Las piezas son sometidas a una cámara de viento para hacer que la pintura se seque rápidamente.
- **Empaque:** Esta etapa se divide en dos. El empaque individual de cada producto y el empaque por lotes para el despacho.
- **Despacho:** El material se prepara y/o almacena hasta que se lleve a los respectivos canales de distribución y comercialización.



#### Etapas con Mejoras en Productividad
 
- **Inyección:** Se opta por usar una celda robotizada con las funciones de extraer las piezas resultantes del proceso de inyección, así como la extracción e instalación de moldes en la inyectora, lo que ahorra tiempos y costos, ya que de forma manual podríamos tener paros en la producción de hasta 6 horas o incluso más, además este proceso participa activamente en la agregación de valor al producto.

- **Desbarbado:** Como es bien conocido, el desbarbado es fundamental para evitar lesiones en las personas que manipulan las piezas, puestas pueden presentar filos e imperfecciones que afecten de una forma otra las tolerancias dimensionales, su apariencia, etc. En los tiempos recientes se ha venido explorado una nueva tecnología de desbarbado criogénico, donde las piezas son expuestas a bajas temperaturas y situadas en un tambor rotatorio, proceso en el que se desprenden las rebabas con espesores menores a 3 mm, lo que se adapta perfectamente a nuestra operación. Esto reduce de forma significativa los tiempos que se necesitan en este proceso, dado que el desbarbado se hace en su mayoría por un operario experto y este pierde su eficiencia a lo largo del turno de trabajo.
  
- **Empaque:** Dado que el empacado por lotes no aporta directamente en la agregación de valor al producto, se optó por automatizar el empacado individual de cada juguete, mediante la aplicación de una celda robotizada. Se usó como inspiración el proceso de de empacado de televisores. 
---

## Celda Robotizada: IRB 6700

El robot desempeña un papel de **Pick and Place**, lo cual es clave en la automatización del proceso de inyección, encargándose de la extracción de piezas y el cambio de moldes en la inyectora. La producción se organiza en ciclos secuenciales para los moldes **Qammar, Propulser y Trompo de Batalla**, alternando su uso tras alcanzar la meta diaria de cada producto.

Para garantizar una operación eficiente y segura, el sistema cuenta con **sensores de colisión** para la detección de herramientas y **sensores de posición** para verificar la correcta instalación de los moldes en la inyectora.

## Procedimiento de Operación

El procedimiento de operación se estructura de la siguiente manera:

1. El robot inicia en **posición de "home"**, con todas las herramientas en la estación de almacenamiento y el **molde Qammar** montado en la inyectora.
2. Se selecciona la herramienta de extracción de piezas y se inicia el ciclo de producción.
3. El robot ejecuta la rutina de extracción tras cada inyección, repitiéndose hasta alcanzar la **meta diaria** del producto.
4. Alcanzado el objetivo, la inyectora se detiene y el robot cambia a la herramienta de manipulación de moldes.
5. Se realiza el **cambio de molde**, verificando su correcta instalación antes de continuar.
6. El proceso se repite para los tres moldes hasta completar la producción diaria.
7. Al finalizar la jornada, el **molde Qammar** queda instalado en la inyectora para el siguiente ciclo.

Este esquema operativo **minimiza tiempos de inactividad y optimiza el uso de los recursos**, asegurando una producción continua y eficiente.

Para garantizar una sincronización precisa entre la extracción de la pieza desde la inyectora y el proceso de inyección, se ha estandarizado el tiempo de ciclo de ambos procesos. Esta sincronización es fundamental para evitar colisiones entre la herramienta y el molde, así como posibles impactos entre las piezas recién inyectadas, el molde o la propia inyectora.


### Layout de la Celda
El ingreso de materia prima a la celda robotizada se realiza a través de un  **Powder Auger Feeder 4**, un alimentador diseñado para la dosificación precisa de material particulado, que puede ser empleado para suministrar material polimérico en formato de pellets. Este sistema permite la incorporación opcional de partículas de colorante para modificar la apariencia del producto final según los requerimientos de producción. La celda està delimitada por la barreras de contenciòn, las cuales suman un àrea de 

![ef1b14b86163f6d00819b97d7a4f8b8f7404c24e](https://github.com/user-attachments/assets/e7ac21cd-bad7-41a6-a6d0-e5537db7067f)

Una vez completado el proceso de inyección, las piezas moldeadas son extraídas y transportadas fuera de la celda para continuar con el proceso de desbarbado, asegurando así su adecuada preparación para el ensamblaje del juguete.

![a88b96ccdf0a5fc9ca29ae0ede7bd0256c92e196](https://github.com/user-attachments/assets/ffae11c4-e3f7-4410-9c99-828adadd2a10)



### Componentes
En esta sección se detallan los elementos que se usarán en las celdas. La selección de los componentes se hizo en base a las normativas **IEC 60204-1** e **ISO 10218-1:2011**.


- **IRB 6700 300-270:** Robot seleccionado para esta tarea, diseñado para mover cargas pesadas (más de 200 kg). Su tamaño le permite alcanzar los elementos y estaciones de la celda sin dificultad, como la estación de herramientas, la banda transportadora y la inyectora.

![image](https://github.com/user-attachments/assets/c2599466-26ac-4dac-937d-9f7e55ccf8df)


- **IRC5 u OmniCore:** Controlador de ABB para integrarse con el IRB 6700.

- **370 E GOLDEN ELECTRIC 2:** Inyectora seleccionada para volúmenes de producción bajos a medios. Destaca por su facilidad en la extracción y cambio de moldes, optimizando el tiempo de producción.

- **Conveyor 950 4000 h2:** Banda transportadora utilizada para la entrada y salida de material en la celda. Su disponibilidad en el catálogo de ABB facilita su integración con el robot.

- **Barreras físicas:** Se debe considerar su robustez, facilidad de instalación y compatibilidad con los componentes de seguridad.

- **Paros de emergencia:** Dispositivo que permite detener el robot de forma inmediata en casos de emergencia. Se selecciona un pulsador normalmente cerrado, ABB Jokab Safety E-Stop Button (SFC-EB3A).

- **Paros de seguridad:** Se integra un relé de seguridad para desconectar el robot de la red eléctrica en caso de fallos. Se selecciona el ABB Jokab Safety Pluto Safety PLC (Pluto S20 v2), que permite diagnósticos en tiempo real y redundancia a fallos críticos.

- **Escáneres Láser:** Detectan la presencia en el área de trabajo de la celda robotizada. Se usa el modelo SICK S3000 Advance, configurable para distintas distancias de detección. Detiene el ciclo de trabajo si detecta a un operador en la celda.

- **Accionamiento:** Se realiza con un tablero de control con paradas de emergencia integradas. También puede usarse en conjunto con FlexPendant de ABB.

- **ABB SafeMove2:** Solución de software y hardware para mejorar la seguridad de los robots ABB, eliminando la necesidad de hardware adicional.

- **Patlite Signal Tower:** Proporciona información visual clara del estado operativo del robot. Se selecciona la LR6 DC-ASSY BUZZER POLE-SZL001 Series 60mm LED Signal Tower Lights, instaladas en cada esquina de la celda.

#### Efectores Finales

Para efectuar el cambio entre moldes, se requiere una herramienta específica que se enrosca en la parte superior del molde. 

Dado que el molde pesa 100 kg, el tornillo debe soportar una carga de 981 N:

$$
F = 981 \text{ N}
$$

El área de la sección transversal del tornillo se calcula como:

$$
A = \frac{\pi}{4} d^2 = \frac{\pi}{4} (30 \text{ mm})^2 = 706.86 \text{ mm}^2
$$

El esfuerzo axial resultante es:

$$
\sigma = \frac{F}{A} = \frac{981}{706.86} = 1.39 \text{ MPa}
$$

Dado que este valor es bajo, pero el entorno industrial puede exponerlo a químicos y humedad, se selecciona **acero inoxidable AISI 316**, que posee una resistencia a fluencia superior a 200-300 MPa, garantizando su resistencia en esta aplicación.

![f7aa2898-fb5e-4e5e-a5b4-a154d49230d9](https://github.com/user-attachments/assets/e07e9394-2c72-4fdd-9254-c7a3aaecb69e)

Para la extracción de las piezas, se opta por una **pinza neumática**.

![ec3173f1-17ac-4edb-bb8b-4776b827fe15](https://github.com/user-attachments/assets/f50d2a13-6d55-46e2-b6f7-5e86100503ac)


- **Estación de herramientas:** Permite el intercambio de herramientas de forma precisa sin intervención humana. Se implementa un sistema basado en el diseñado por Jorge Yagüez Aparicio en la Universidad Carlos III.

Como sìntesis de lo anterior, se muestra la tabla de componentes de la celda:

| Cantidad | Componente |
|----------|--------------------------------|
| 1        | **Robot Industrial** - ABB IRB 6700 300-270 |
| 1        | **Controlador** - ABB IRC5 u OmniCore |
| 1        | **Inyectora** - 370 E GOLDEN ELECTRIC 2 |
| 2        | **Banda Transportadora** - Conveyor 950 4000 h2 |
| 1        | **Alimentador de Polímero** - Powder Auger Feeder 4 |
| 31       | **Barreras de Seguridad** - Vallado Serie 2000 de FERAX |
| 3        | **Escáner Láser** - SICK S3000 Advance |
| 2        | **Paro de Emergencia** - ABB Jokab Safety E-Stop SFC-EB3A |
| 1        | **PLC de Seguridad** - ABB Jokab Pluto S20 v2 |
| 1        | **Software de Seguridad** - ABB SafeMove2 |
| 4        | **Sistema de Señalización** - Patlite Signal Tower LR6 |

### Duty Cycle y Throughput Time
En la plataforma de RobotStudio se cronometró el tiempo  para la rutina de cambio de moldes y para la extracción de la pieza de la inyectora. En el caso de extracción de piezas el duty cycle y el throughtput time.  


| Rutina         | Duty Cycle |
|---------------|------------|
| Extracción    | 10.9 s |
| Cambio de Moldes | 52.0 s |


# Agregación de Valor de la Celda Robotizada

- *Reducción de tiempos de inactividad:* La automatización del cambio de moldes disminuye el tiempo de configuración de **2-3 horas a 1 minuto**, aumentando la disponibilidad de la inyectora y eliminando retrasos en la producción.

- *Optimización del consumo energético:* La consolidación de inyectoras permite operar con una menor cantidad de equipos, **reduciendo significativamente el consumo eléctrico** y los costos de mantenimiento asociados.

- *Incremento en la eficiencia operativa:* La extracción automatizada de piezas y la reducción de tiempos de ciclo permiten producir un mayor número de juguetes por día, **eliminando cuellos de botella y mejorando la planificación de producción**.

- **Disminución de desperdicios y reprocesos:* La precisión del robot en la manipulación de moldes y piezas **minimiza errores en la inyección**, reduciendo pérdidas por defectos y optimizando el uso del material.




---

## Identificación de Peligros y Gestión de Riesgos

Con la lectura y revisión del  Apéndice A de la norma ISO 10218-1:2011, se identificaron los siguientes riesgos en la celda.


### Riesgos Presentes
- Contacto accidental con el robot.
- Fallo en la función de paro de seguridad.
- Caída del molde.
- Colisión del robot con la inyectora.
- Exposición a temperaturas extremas y material fundido.
- Pinzamiento en el manipulador del robot.
- Fallo en el sistema de control de seguridad.
- Liberación accidental de los frenos del robot.
- Manipulación inadecuada del equipo en mantenimiento.
- Atrapamiento en las bandas transportadoras.




### Medidas de Mitigación
- Instalación de **barreras físicas y sensores de seguridad**.
- Implementación de **sistemas de paro de emergencia**.
- Mantenimiento preventivo en sistemas de fijación y frenos.
- Capacitación del personal en protocolos de seguridad.

## Frecuencia y Probabilidad de los Peligros

Para la estimación de riesgos, se utilizó el puntaje **HRN**. Muchos de los componentes ya están diseñados para prevenir estos riesgos. Por ejemplo, la cortina láser desactiva el manipulador cuando detecta el ingreso de personal a la celda, evitando lesiones o accidentes fatales.

### Evaluación de Riesgos HRN

| **Riesgo** | **Probabilidad** | **Severidad** | **HRN** |
|------------|----------------|--------------|---------|
| Contacto accidental con el robot | 3 | 4 | 12 |
| Fallo en la función de paro de seguridad | 2 | 5 | 10 |
| Caída del molde | 3 | 4 | 12 |
| Colisión del robot con la inyectora | 2 | 4 | 8 |
| Exposición a temperaturas cambiantes y material fundido | 3 | 3 | 9 |
| Pinzamiento entre la caja y el manipulador del robot | 3 | 3 | 9 |
| Fallo en el sistema de control de seguridad | 1 | 5 | 5 |
| Liberación de los frenos del robot | 2 | 4 | 8 |
| Manipulación inadecuada del equipo durante el mantenimiento | 3 | 3 | 9 |
| Atrapamiento en las bandas transportadoras | 1 | 4 | 15 |

---

## Escala de Probabilidad (P)

| **Valor** | **Descripción** |
|-----------|----------------|
| 1 | Muy baja – Ocurre en condiciones excepcionales. |
| 2 | Baja – Posible en circunstancias poco frecuentes. |
| 3 | Media – Puede ocurrir ocasionalmente. |
| 4 | Alta – Probable en operación normal. |
| 5 | Muy alta – Casi seguro que ocurrirá en operación normal. |

---

## Escala de Severidad (S)

| **Valor** | **Descripción** |
|-----------|----------------|
| 1 | Insignificante – Sin consecuencias o solo molestias menores. |
| 2 | Leve – Daños leves, sin incapacidad significativa. |
| 3 | Moderado – Lesiones tratables, incapacidad temporal. |
| 4 | Grave – Lesiones serias, posible incapacidad permanente. |
| 5 | Catastrófico – Muerte o lesiones irreversibles. |

---

## Clasificación del Nivel de Riesgo (HRN)

| **Puntaje HRN** | **Nivel de Riesgo** |
|-----------------|---------------------|
| 1 - 4 | Bajo – No requiere medidas especiales más allá de la supervisión operativa. |
| 5 - 9 | Moderado – Se recomienda implementar medidas de mitigación y supervisión. |
| 10 - 15 | Alto – Es obligatorio implementar medidas de seguridad estrictas. |
| 16 - 25 | Crítico – Riesgo inaceptable, es necesario rediseñar la celda o el proceso. |


## Mitigación de los Peligros

Se debe determinar cuáles riesgos requieren la incorporación de componentes de seguridad y cuáles pueden mitigarse mediante manuales, entrenamiento y el uso de Equipos de Protección Personal (EPP).

### 1. Contacto accidental con el robot
- Incorporar dispositivos de detección, como escáneres láser y cortinas de luz.
- Instalar barreras físicas o protecciones móviles en el área de trabajo.
- Establecer procedimientos de capacitación y uso de EPP para los operarios.

### 2. Fallo en la función de paro de seguridad
- Utilizar relés de seguridad redundantes.
- Realizar mantenimientos preventivos y pruebas periódicas del sistema de paro.
- Asegurar la integración y verificación continua del sistema de seguridad en el controlador.

### 3. Caída del molde
- Emplear dispositivos de sujeción robustos (abrazaderas o sistemas de fijación específicos).
- Integrar sensores de posición que confirmen la sujeción correcta antes de iniciar movimientos.

### 4. Colisión del robot con la inyectora
- Establecer límites programados de seguridad y zonas restringidas mediante SafeMove2.
- Instalar barreras físicas y sensores de proximidad para prevenir acercamientos peligrosos.
- Realizar simulaciones en RobotStudio para validar las trayectorias.

### 5. Exposición a temperaturas cambiantes y a material fundido de la inyectora
- Proveer barreras térmicas y señalización que advierta sobre zonas calientes.
- Suministrar EPP específico (guantes resistentes al calor, protección facial, ropa térmica) en caso de que se necesite entrar a la celda.

### 6. Pinzamiento entre los moldes y el manipulador del robot
- Establecer controles de acceso y paros de emergencia específicos.
- Integrar sensores de colisión en áreas de posible impacto para detener el proceso.

### 7. Fallo en el sistema de control de seguridad
- Emplear un PLC de seguridad redundante.
- Realizar pruebas de diagnóstico en tiempo real y mantenimiento preventivo.
- Incluir simulaciones en RobotStudio para validar el sistema antes de su operación.

### 8. Liberación de los frenos del robot
- Incorporar un sistema de frenos redundante y realizar inspecciones periódicas.
- Asegurar procedimientos de puesta en marcha y verificación antes de iniciar operaciones.
- Capacitar al personal de mantenimiento en la operación y verificación de los frenos.

### 9. Manipulación inadecuada del equipo durante el mantenimiento
- Desarrollar y seguir procedimientos de mantenimiento estandarizados.
- Proveer entrenamiento regular y el uso de EPP adecuado (guantes, protección ocular y ropa de seguridad).
- Implementar supervisión en las actividades de mantenimiento.

### 10. Atrapamiento en las bandas transportadoras
- Instalar protecciones fijas y móviles en las bandas transportadoras.
- Integrar sensores de seguridad y paros de emergencia en la línea de producción.




---

## Referencias
1. ABB. *Robotics IRB 6700: The 7th generation of large industrial robots*.
2. EUCHNER. *Seguridad en celdas robóticas ISO 10218*.
3. Jiafan Zhang & Xinyu Fang. *Challenges in robotic cell layout optimization*.
4. Richard Muther Associates. *How to Plan a Manufacturing Cell*.

---

Este archivo en Markdown mantiene la estructura del documento original y está optimizado para ser leído en **GitHub**. Si necesitas modificaciones o agregar imágenes, házmelo saber. 🚀
