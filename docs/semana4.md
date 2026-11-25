# Análisis de mercado y propuesta de valor

!!! info "Objetivo de la semana"
    Definir el mercado al que se dirige Nervik, identificar al comprador y al usuario, estimar su tamaño, comparar las soluciones existentes y formular una propuesta de valor que justifique por qué una empresa de transporte elegiría nuestro producto.

---

## 1. Introducción

Durante esta semana pasamos del análisis de propiedad intelectual a estudiar la oportunidad comercial de **Nervik**, nuestro sistema de detección y registro de anomalías para vehículos de transporte de carga.

Uno de los principales aprendizajes fue comprender que desarrollar una solución tecnológica no garantiza que exista un mercado dispuesto a comprarla.

Por esta razón, analizamos quién enfrenta el problema, cuánto le cuesta, qué alternativas utiliza actualmente y qué beneficio concreto podría ofrecer nuestro dispositivo.

La intención no fue únicamente encontrar posibles clientes, sino identificar un segmento suficientemente específico para diseñar el producto de acuerdo con sus necesidades.

---

## 2. Continuidad con la Semana 3

En la semana anterior seleccionamos el nombre Nervik y comenzamos a estudiar tecnologías relacionadas con la seguridad de vehículos, la detección de interferencias y el monitoreo de flotas.

También identificamos la importancia de mantener el sistema como un dispositivo de **lectura, detección y registro**, evitando intervenir directamente en los controles del camión.

| Aspecto | Resultado |
|:---|:---|
| Marca seleccionada | Nervik |
| Enfoque del producto | Detección y registro de anomalías |
| Libertad de operación | Riesgo medio preliminar |
| Decisión técnica relevante | Lectura CAN/J1939 sin intervenir en el vehículo |
| Entrevistas | Validación todavía limitada |
| Siguiente pregunta | ¿Quién compraría Nervik y por qué? |

Estas decisiones sirvieron como punto de partida para el análisis comercial.

---

## 3. Definición del segmento de mercado

Para definir nuestro cliente utilizamos el concepto de **segmento accionable**, que consiste en identificar un grupo específico de compradores con necesidades, comportamientos y capacidad de compra similares.

El equipo concentró su análisis en empresas mexicanas de transporte de carga que operan flotas medianas y utilizan rutas con riesgos de robo o pérdida de comunicación.

### 3.1 Segmento seleccionado

!!! success "Segmento objetivo"
    Empresas mexicanas de transporte con flotas de **31 a 100 unidades**, especialmente aquellas que transportan carga asegurada por los corredores México–Puebla–Veracruz y México–Querétaro–Bajío.

    Son organizaciones que ya utilizan GPS y servicios de monitoreo, pero que pueden perder visibilidad cuando sus vehículos enfrentan interferencias de comunicación.

### 3.2 Perfil del cliente en cuatro capas

Se utilizó Claude como apoyo para organizar el perfil en cuatro dimensiones, diferenciando la información sustentada por fuentes de las hipótesis que requieren entrevistas.

| Capa | Características del segmento | Estado |
|:---|:---|:---|
| Demográfica | Empresas de transporte con 31–100 unidades que operan en México | Segmento definido |
| Demográfica | Operación frecuente por corredores del centro del país | Enfoque geográfico propuesto |
| Conductual | Contratan rastreo GPS, monitoreo y, en algunos casos, custodia | Documentado en investigación del equipo |
| Conductual | Durante una interrupción pueden depender de alertas recibidas por la central | Requiere validación por empresa |
| Psicográfica | Preocupación por perder visibilidad e información durante incidentes | Hipótesis de usuario |
| Psicográfica | Interés en reducir la incertidumbre durante un posible robo | Evidencia parcial |
| Económica | Ya existe gasto en rastreo, monitoreo y seguridad | Documentado en análisis competitivo |
| Económica | Posible disposición a pagar una suscripción adicional | Hipótesis pendiente de validar |

### 3.3 Usuario, comprador y decisor

Es importante diferenciar a las personas que utilizarían la información de Nervik de quienes autorizarían su adquisición.

| Rol | Perfil |
|:---|:---|
| Usuario principal | Operador del centro de monitoreo o responsable de revisar alertas |
| Comprador | Gerente de seguridad o de operaciones |
| Decisor | Dueño o director de la empresa transportista |
| Influenciador | Aseguradora o intermediario de seguros de carga |

Esta separación es relevante porque el usuario necesita información comprensible y oportuna, mientras que el comprador debe justificar económicamente la inversión.

### 3.4 Problema principal

Los sistemas de rastreo permiten conocer la posición de las unidades mientras existe comunicación.

Sin embargo, cuando se pierde conectividad, puede existir un periodo sin información suficiente sobre lo que ocurrió.

La oportunidad identificada por el equipo consiste en desarrollar un dispositivo que **continúe registrando información localmente**, aunque no pueda transmitirla de inmediato.

!!! note "Interpretación personal"
    Desde la perspectiva de ingeniería, esto significa que Nervik no debería depender por completo de un servidor remoto para analizar los sensores.

    El microcontrolador necesita ejecutar funciones locales de detección y registro. Así, cuando se restablezca la comunicación, el sistema podría recuperar y enviar los eventos almacenados.

---

## 4. Tipos de valor: Pirámide de Bain e IDEO

Durante la sesión revisamos que un producto puede entregar diferentes tipos de valor al usuario.

Para Nervik identificamos principalmente beneficios funcionales y emocionales.

### 4.1 Aplicación de la Pirámide de Bain

| Nivel de valor | Aplicación en Nervik |
|:---|:---|
| Funcional | Registrar información, detectar anomalías y facilitar la revisión de incidentes |
| Emocional | Reducir la incertidumbre del responsable de seguridad |
| Transformador | Mejorar la manera en que una empresa documenta e investiga incidentes, si se valida su utilidad |

El valor funcional es el más importante en nuestra etapa de desarrollo porque puede convertirse en requisitos medibles del producto.

El nivel emocional representa una oportunidad posterior: ofrecer mayor tranquilidad a quienes tienen la responsabilidad de supervisar una flota.

### 4.2 Evaluación con el marco IDEO

El marco IDEO permite analizar si una propuesta ofrece información relevante sobre el usuario, diferenciación y un enfoque claro.

| Criterio | Evaluación | Justificación |
|:---|:---:|:---|
| Insightful | ✅ | Se enfoca en la falta de información durante un incidente |
| Unique | ⚠️ | Existen competidores que también detectan interferencias |
| Targeted | ✅ | El producto se dirige a flotas medianas en corredores de riesgo |

!!! warning "Aspecto pendiente"
    La diferenciación de Nervik todavía necesita comprobarse.

    No basta con afirmar que otros sistemas dejan de funcionar cuando pierden señal. Es necesario comparar sus capacidades reales de detección, almacenamiento local y recuperación de eventos.

---

## 5. Tamaño de mercado: TAM, SAM y SOM

Para estudiar el potencial comercial utilizamos tres indicadores:

- **TAM:** mercado total que podría atender la solución.
- **SAM:** parte del mercado a la que podríamos dirigirnos con nuestro modelo de negocio.
- **SOM:** participación que sería razonable intentar conseguir durante los primeros años.

El equipo utilizó información de la Dirección General de Autotransporte Federal de la SICT y supuestos de segmentación para construir una estimación inicial.

### 5.1 Supuesto económico

Se planteó un modelo de suscripción de:

**$300 MXN mensuales por unidad.**

Esto representa:

**$300 × 12 = $3,600 MXN anuales por unidad.**

Este precio es un supuesto comercial y no una disposición de pago confirmada mediante entrevistas suficientes.

### 5.2 Mercado total — TAM

El escenario utilizado parte de aproximadamente **249,180 tractocamiones** pertenecientes a empresas con 31 o más unidades.

Cálculo:

**249,180 × $3,600 = $897,048,000 MXN anuales.**

### 5.3 Mercado atendible — SAM

Se delimitó el mercado a las flotas medianas, considerando un subconjunto de vehículos que podría operar en corredores del centro del país.

El equipo utilizó un filtro de exposición del 50%, que todavía debe validarse.

Resultado estimado:

**46,023 unidades × $3,600 = $165,682,800 MXN anuales.**

### 5.4 Mercado obtenible — SOM

Para los primeros dos años se utilizó un escenario comercial de:

- Año 1: 110 unidades.
- Año 2: 300 unidades adicionales.
- Total acumulado: 410 unidades.

Ingreso recurrente anual hipotético, si las 410 unidades permanecen activas:

**410 × $3,600 = $1,476,000 MXN.**

### 5.5 Resumen del dimensionamiento

| Indicador | Unidades estimadas | Valor anual aproximado |
|:---|---:|---:|
| TAM | 249,180 | $897 millones MXN |
| SAM | 46,023 | $166 millones MXN |
| SOM (acumulado en dos años) | 410 | $1.48 millones MXN |

!!! warning "Limitaciones del cálculo"
    El escenario procede del análisis preliminar del equipo basado en cifras SICT/DGAF de mayo de 2026.

    El porcentaje de exposición a corredores de riesgo, la adopción comercial y el precio mensual son supuestos. Las estimaciones no deben interpretarse como ventas garantizadas.

### 5.6 Interpretación de resultados

El análisis indica que existe un segmento potencial para un dispositivo complementario de seguridad vehicular.

Sin embargo, el SOM es considerablemente menor que el TAM, lo que muestra la importancia de seleccionar clientes específicos y desarrollar una estrategia de comercialización alcanzable.

También identificamos que la viabilidad económica sería limitada durante los primeros años si los ingresos solamente provienen de una suscripción pequeña y el equipo requiere cubrir todos sus gastos operativos.

---

## 6. Análisis competitivo

Para comprender las alternativas existentes se realizó una investigación con apoyo de Perplexity y Claude.

Separamos las opciones en tres categorías:

1. Competidores directos.
2. Competidores indirectos.
3. Sustitutos del producto.

### 6.1 Mapa competitivo

| Tipo | Alternativa | Qué ofrece | Aspecto que debemos comparar |
|:---|:---|:---|:---|
| Directo | Motive | Telemática y determinadas alertas de interferencia | Operación y registro durante pérdida de señal |
| Directo | Black GPS | Localización y monitoreo vehicular | Capacidades de almacenamiento y evidencia |
| Directo | MexTracker / anti-jammer | Detección de interferencias y respuestas de seguridad | Diferencia entre detectar, registrar e intervenir |
| Indirecto | Geotab | Información del vehículo y gestión de flotas | Alcance funcional y complejidad |
| Indirecto | Samsara | Telemática, monitoreo y gestión | Costos y continuidad de registros |
| Indirecto | GPS con central 24/7 | Seguimiento remoto y atención de alertas | Información disponible sin conectividad |
| Sustituto | Custodia física | Vigilancia durante el traslado | Costo por viaje y capacidad de cobertura |
| Sustituto | Convoyes y horarios restringidos | Reducción de exposición al riesgo | Impacto operativo |

Los competidores no son necesariamente inferiores en todas sus funciones. Por esta razón, sus capacidades deben confirmarse mediante fichas técnicas y pruebas comparables.

### 6.2 Competidor más difícil de desplazar

Consideramos que una de las alternativas más difíciles de sustituir es el **GPS convencional acompañado de una central de monitoreo**, porque muchas transportistas ya lo utilizan como parte de sus procedimientos de seguridad.

Por lo tanto, Nervik no debería presentarse como reemplazo completo del monitoreo actual.

Una alternativa comercial sería ofrecerlo como una **capa adicional de registro y análisis local**.

### 6.3 Conclusión competitiva

Nuestra oportunidad no está únicamente en detectar interferencias.

El atributo que el equipo busca diferenciar es la capacidad de conservar información durante la interrupción y generar un expediente consultable posteriormente.

Todavía es necesario comprobar la utilidad de esa evidencia con usuarios y aseguradoras.

---

## 7. Mapa de posicionamiento

El posicionamiento propuesto utiliza dos variables:

- **Costo mensual por unidad.**
- **Capacidad de registrar eventos durante la pérdida de comunicación.**

| Alternativa | Costo relativo | Autonomía sin comunicación |
|:---|:---|:---|
| GPS convencional | Bajo a medio | Por verificar según equipo |
| Telemática avanzada | Medio a alto | Variable según plataforma |
| Sistemas anti-jammer | Variable | Variable según fabricante |
| Custodia física | Alto por viaje | No depende del GPS para acompañar físicamente |
| Nervik (objetivo) | Medio | Alta capacidad de registro local prevista |

!!! info "Posicionamiento buscado"
    Nervik pretende ofrecer una función de registro local complementaria al sistema de rastreo existente, sin necesidad de controlar directamente el vehículo.

    Esta posición corresponde al diseño propuesto; todavía debe demostrarse mediante pruebas funcionales.

---

## 8. Estrategia Blue Ocean

La estrategia Blue Ocean busca encontrar atributos que permitan diferenciar una propuesta en lugar de competir únicamente por precio o por cantidad de funciones.

Para ello utilizamos el marco de cuatro acciones.

### 8.1 Eliminar, reducir, incrementar y crear

| Acción | Decisión propuesta | Justificación |
|:---|:---|:---|
| Eliminar | Intervención directa sobre el motor | Mantener un sistema de lectura y registro |
| Reducir | Funciones de gestión general de flotas | Concentrarse en detección y evidencia |
| Incrementar | Procesamiento local de señales | Reducir dependencia del servidor |
| Incrementar | Registro durante pérdida de conectividad | Conservar información relevante |
| Crear | Expediente verificable del incidente | Facilitar investigación posterior |

### 8.2 Lienzo estratégico

La siguiente tabla es una comparación cualitativa preliminar en escala de 1 a 5.

Los valores son puntuaciones del modelo estratégico trabajado por el equipo, no resultados de pruebas independientes.

| Atributo | Custodia | Telemática | GPS anti-jammer | Nervik propuesto |
|:---|:---:|:---:|:---:|:---:|
| Costo relativo (5 = más caro) | 5 | 4 | 2 | 2 |
| Funciones de eficiencia | 1 | 5 | 2 | 1 |
| Operación sin señal | 4 | 1 | 2 | 5 |
| Evidencia verificable | 2 | 2 | 1 | 5 |
| Facilidad de instalación | 2 | 3 | 3 | 4 |
| Flexibilidad comercial | 3 | 1 | 3 | 4 |
| Intervención física | 5 | 1 | 3 | 1 |

### 8.3 Oportunidad identificada

El espacio de diferenciación que proponemos consiste en registrar información útil en momentos en los que otros sistemas no pueden transmitirla.

Esta característica puede resultar valiosa para reconstruir un incidente, pero todavía se debe confirmar si los responsables de seguridad y las aseguradoras estarían dispuestos a pagar por ella.

!!! note "Relación con la ingeniería"
    La estrategia Blue Ocean también influye en las decisiones técnicas.

    Si nuestra diferenciación es el registro local, el diseño debe contemplar memoria, respaldo de energía, procesamiento independiente de la nube y mecanismos para conservar la integridad de los eventos.

    Estas características deberán convertirse posteriormente en requisitos medibles del PDS.

---

## 9. Construcción de la propuesta de valor

Después de definir el segmento, el mercado y los competidores, utilizamos Claude para explorar diferentes formas de comunicar el beneficio del producto.

La actividad buscó evitar descripciones enfocadas exclusivamente en componentes, sensores o algoritmos.

### 9.1 Tres versiones

| Versión | Propuesta |
|:---|:---|
| Funcional | Nervik busca continuar registrando anomalías incluso cuando un vehículo pierde comunicación con su sistema de monitoreo. |
| Emocional | Nervik busca reducir la incertidumbre del responsable de seguridad al conservar información útil durante una interrupción. |
| Integrada | Para flotas medianas en rutas de riesgo, Nervik busca conservar evidencia local de anomalías cuando se interrumpe la comunicación del vehículo. |

### 9.2 Propuesta seleccionada

!!! success "Propuesta de valor de Nervik"
    **Para flotas medianas en corredores de riesgo, Nervik busca conservar evidencia local de anomalías durante interrupciones de comunicación, facilitando la investigación posterior de incidentes.**

Esta versión combina tres elementos:

- Identifica al cliente objetivo.
- Describe el resultado que busca obtener.
- Explica la diferenciación propuesta sin limitarse a enumerar componentes.

### 9.3 Oferta frente a propuesta de valor

| Concepto | Descripción |
|:---|:---|
| Oferta | Dispositivo electrónico con GNSS, IMU, CAN/J1939, comunicación celular y procesamiento local |
| Propuesta de valor | Conservar información útil cuando el monitoreo remoto pierde conectividad |

La oferta explica qué se está desarrollando.

La propuesta de valor explica por qué ese desarrollo podría resultar importante para el comprador.

### 9.4 Validación inicial

La documentación del equipo incluye la opinión favorable de un transportista de carga perecedera que había experimentado incidentes de robo.

Esa conversación aportó una señal preliminar de interés por la seguridad y por un modelo de suscripción.

Sin embargo, una sola opinión no permite establecer la disposición a pagar de todo el mercado ni confirmar que las aseguradoras reconocerían el expediente generado.

Por ello, se requieren entrevistas estructuradas adicionales.

---

## 10. Canvas de mercado — Nervik

El Canvas de mercado resume las decisiones principales de esta semana.

| Elemento | Síntesis |
|:---|:---|
| Segmento | Transportistas medianas de 31–100 unidades en rutas de riesgo |
| Usuario | Personal de monitoreo y seguridad |
| Comprador | Gerente de seguridad u operaciones |
| Decisor | Dueño o director de la transportista |
| Problema | Pérdida de información durante interrupciones de señal |
| TAM | 249,180 unidades; aproximadamente $897 M MXN/año |
| SAM | 46,023 unidades; aproximadamente $166 M MXN/año |
| SOM | 410 unidades acumuladas en dos años |
| Competencia | Rastreo GPS, telemática, anti-jammer y custodia |
| Diferenciación propuesta | Registro local y recuperación de eventos |
| Blue Ocean | Evidencia del incidente durante pérdida de conectividad |
| Propuesta de valor | Conservar información útil para investigar anomalías |
| Precio hipotético | $300 MXN por unidad al mes |
| Principal riesgo | Que el comprador no valore suficientemente la evidencia registrada |

### Hipótesis pendientes

1. Frecuencia real de interrupciones de señal por flota.
2. Disposición a pagar por una capa adicional de registro.
3. Utilidad y aceptación del expediente por parte de aseguradoras.
4. Capacidad real del hardware para detectar y conservar eventos.
5. Ventaja demostrable frente a las soluciones actuales.

---

## 11. Resultados de la semana

| Actividad | Resultado |
|:---|:---|
| Definición del segmento | Flotas medianas en corredores de riesgo |
| Perfil de usuario | Cuatro capas documentadas |
| Tipos de valor | Funcional y emocional |
| TAM/SAM/SOM | Escenario preliminar elaborado |
| Análisis competitivo | Competidores directos, indirectos y sustitutos |
| Blue Ocean | Registro local y evidencia como diferenciadores |
| Propuesta de valor | Versión enfocada en el resultado del cliente |
| Canvas de mercado | Síntesis elaborada |
| Validación directa | Parcial; requiere más entrevistas |

---

## 12. Reflexión personal

Esta semana comprendí que la viabilidad de un proyecto de ingeniería no depende únicamente de que podamos construirlo.

En Nervik, inicialmente resulta atractivo hablar de sensores, comunicación celular, inteligencia artificial y lectura del vehículo. Sin embargo, estas características no explican por sí mismas por qué una empresa decidiría comprarlo.

El análisis de mercado me permitió entender que el valor debe relacionarse con una necesidad específica del usuario.

Desde mi perspectiva, la decisión más importante es mantener la capacidad de procesamiento y registro local, ya que ese atributo está directamente relacionado con el problema que buscamos atender.

También identifiqué que una propuesta comercial debe sustentarse con pruebas. Aunque podemos plantear una diferenciación frente al rastreo convencional, necesitamos demostrarla con el prototipo y comprobar si realmente representa un beneficio para las transportistas.

---
