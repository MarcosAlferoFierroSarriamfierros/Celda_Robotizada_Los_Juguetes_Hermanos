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

### Layout de la Celda
El **Powder Auger Feeder 4** alimenta la celda con pellets de ABS, permitiendo la adición de colorantes. Tras la inyección, las piezas son extraídas automáticamente y enviadas al **proceso de desbarbado**.

### Componentes
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
| Rutina         | Duty Cycle |
|---------------|------------|
| Extracción    | 10.9 s |
| Cambio de Moldes | 52.0 s |

---

## Identificación de Peligros y Gestión de Riesgos

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

### Clasificación del Nivel de Riesgo (HRN)
| Riesgo | Probabilidad | Severidad | HRN |
|--------|-------------|-----------|-----|
| Contacto con el robot | 3 | 4 | 12 |
| Fallo en paro de seguridad | 2 | 5 | 10 |
| Caída del molde | 3 | 4 | 12 |
| Colisión con la inyectora | 2 | 4 | 8 |
| Exposición a material fundido | 3 | 3 | 9 |
| Pinzamiento en el robot | 3 | 3 | 9 |
| Fallo en el control de seguridad | 1 | 5 | 5 |
| Liberación de frenos | 2 | 4 | 8 |
| Errores en mantenimiento | 3 | 3 | 9 |
| Atrapamiento en bandas transportadoras | 4 | 4 | 16 |

### Medidas de Mitigación
- Instalación de **barreras físicas y sensores de seguridad**.
- Implementación de **sistemas de paro de emergencia**.
- Mantenimiento preventivo en sistemas de fijación y frenos.
- Capacitación del personal en protocolos de seguridad.

---

## Referencias
1. ABB. *Robotics IRB 6700: The 7th generation of large industrial robots*.
2. EUCHNER. *Seguridad en celdas robóticas ISO 10218*.
3. Jiafan Zhang & Xinyu Fang. *Challenges in robotic cell layout optimization*.
4. Richard Muther Associates. *How to Plan a Manufacturing Cell*.

---

Este archivo en Markdown mantiene la estructura del documento original y está optimizado para ser leído en **GitHub**. Si necesitas modificaciones o agregar imágenes, házmelo saber. 🚀
