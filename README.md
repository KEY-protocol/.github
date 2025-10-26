# KEY: La Infraestructura de Confianza para el Ecosistema de Inversión de Impacto

**Para:** Project Brief para la Hackatón

**Asunto:** Construye la plataforma de Monitoreo, Reporte y Verificación (MRV) que alinea a financiadores y ejecutores, potenciando el impacto a través de la transparencia colaborativa.

---

## 1. La Visión: De la Carga Administrativa a la Inteligencia de Impacto

Cada año, instituciones como el Banco Mundial, el BID y la ONU invierten miles de millones en programas de desarrollo. Para gestionar estos fondos, las ONGs ejecutoras en el terreno dedican hasta un 30% de sus recursos a tareas de Monitoreo y Evaluación (M&E). El sistema actual exige este laborioso proceso de reporte manual, lo que desvía un tiempo valioso que los equipos podrían dedicar a su misión en el terreno y, a su vez, retrasa la llegada de datos clave a los financiadores.

**KEY Protocol es la solución.** Estamos construyendo una infraestructura de software compartida que automatiza la verificación de resultados, liberando a las ONGs de la carga administrativa y ofreciendo a los financiadores una visibilidad clara y en tiempo real del progreso.

**La Misión de esta Hackatón:** Construir los componentes fundacionales del MVP que presentaremos a nuestros clientes (financiadores) como una herramienta para optimizar toda la cadena de valor del impacto, fortaleciendo su relación con sus socios ejecutores (ONGs).

---

## 2. El Desafío Sistémico: Una Oportunidad Compartida

El sistema actual de reporte no sirve eficientemente a ninguna de las partes. Es una oportunidad para la optimización.

#### Para el Financiador (BID, ONU, etc.):
* **Visibilidad Diferida:** Las decisiones se basan en datos que llegan con semanas o meses de retraso, limitando la capacidad de ajustar estrategias ágilmente.
* **Datos Desestructurados:** Cada socio reporta en formatos distintos, haciendo la comparación y el análisis a nivel de portafolio una tarea compleja y manual.
* **Altos Costos de Auditoría:** La verificación de los reportes es un proceso costoso y lento.

#### Para el Socio Ejecutor (La ONG en Terreno):
* **Enorme Carga de Reporte:** Técnicos y capacitadores altamente cualificados dedican un tiempo precioso a llenar planillas y redactar informes, en lugar de estar con las comunidades.
* **Herramientas Inadecuadas:** A menudo deben usar sistemas que no están diseñados para las condiciones del terreno (baja conectividad, interfaces complejas).
* **Dificultad para Demostrar Valor:** Es un reto comunicar la profundidad y calidad de su trabajo a través de métricas cuantitativas en una hoja de cálculo.

**Nuestra Tesis:** Una plataforma compartida de datos verificables crea un círculo virtuoso. Cuando el reporte se automatiza y se vuelve confiable, los financiadores ganan la visibilidad que necesitan y las ONGs recuperan el tiempo y los recursos para enfocarse en lo que mejor saben hacer: generar impacto.

---

## 3. Arquitectura Propuesta: Grado Institucional desde el Día Cero

* **Capa de Contratos Inteligentes:** Desplegar en una parachain WASM como **Astar Network** (usando `ink!`) o EVM en **Moonbeam** (Solidity).
* **Identidad Soberana:** Integración con **KILT Protocol** para gestionar las identidades digitales de Financiadores, ONGs y Productores.
* **Almacenamiento de Pruebas:** Los metadatos y pruebas (fotos, coordenadas GPS) se almacenarán en **IPFS/Crust**.
* **Frontend:** Dos interfaces clave: una PWA para uso en campo y un Dashboard web para análisis.

---

## 4. Los Desafíos: Tracks de Construcción del MVP

### TRACK A: El Núcleo del Protocolo (Backend / Smart Contracts)

**Bounty 1: Módulo de Identidad y Roles (RBAC).**
* **Misión:** Diseñar un contrato que gestione identidades (DIDs) y asigne roles: `FINANCIADOR`, `ONG_ACREDITADA`, `TÉCNICO_VERIFICADOR`, y `PRODUCTOR`. El rol `PRODUCTOR` será inicialmente pasivo y su identidad será custodiada por la ONG. El sistema debe gestionar las relaciones (ej. qué técnico puede emitir certificados para qué grupo de productores).
* **Importancia:** Es la base para una plataforma segura que refleja las relaciones de confianza y las responsabilidades del mundo real.

**Bounty 2: Contrato de Proyecto y Verificación de Hitos (MRV Core).**
* **Misión:** Desarrollar el contrato que permite a un `FINANCIADOR` definir un "Proyecto" y a un `TÉCNICO_VERIFICADOR` registrar "Hitos" (la emisión de un Certificado de Habilidad) en nombre de un `PRODUCTOR`. Cada hito debe actualizar el estado del proyecto de forma automática.
* **Bonus:** Implementar una lógica de "Financiación por Resultados".

### TRACK B: Las Interfaces de Usuario (Frontend / UX) - El Desafío Clave de Usabilidad

**Bounty 3: La Herramienta de Campo (Field Empowerment App).**
* **Misión:** Prototipar una PWA diseñada para el técnico de campo, asumiendo que el productor no tiene dispositivo ni conectividad. La app debe ser la interfaz de confianza entre el mundo físico y el digital.
* **Flujo Crítico a Diseñar:**
    1.  **Creación de Identidad del Productor:** El técnico registra por primera vez a un productor en el sistema, generando su identidad digital (DID) y una "mochila digital" que será custodiada por la ONG.
    2.  **Selección de Actividad:** El técnico elige el proyecto y la capacitación que está certificando.
    3.  **Emisión y Asignación del Certificado:** El técnico selecciona al productor (o a un grupo de productores) y emite el "Certificado de Habilidad" directamente a su "mochila digital" custodiada. Esta acción es la validación.
* **Desafío Adicional (Conceptual):** ¿Cómo podemos incorporar un mecanismo simple de "Prueba de Presencia" para asegurar el consentimiento y la veracidad, sin requerir acción del productor? (Ej. toma de fotografía con geo-tag y timestamp, cuyo hash se adjunta como metadato).
* **Importancia:** Esta es la pieza más crítica. Si el flujo en el terreno no es impecable, el sistema no puede funcionar.

**Bounty 4: El Dashboard de Inteligencia de Impacto (Funder's Dashboard).**
* **Misión:** Diseñar un dashboard web para un director de programas. Debe transformar los datos (generados por los técnicos en la app de campo) en información estratégica.
* **Visualizaciones Clave:** Vista de portafolio, métricas de cumplimiento, fondos vs. resultados, capacidad de "drill-down" para auditoría.
* **Importancia:** Esta es la interfaz que venderá el proyecto a los financiadores.

### TRACK C: Gobernanza y Futuro del Ecosistema

**Bounty 5: Diseño del Modelo de Gobernanza (La DAO de KEY).**
* **Misión:** Proponer una estructura para la futura DAO que gobernará el protocolo KEY. Esto es un desafío de diseño de sistemas, no solo de código.
* **Preguntas a Responder:**
    * **Membresía y Voto:** ¿Cómo se unen los `FINANCIADORES`, `ONGs` y `TÉCNICOS` a la DAO? ¿Cómo se distribuye el poder de voto para mantener un equilibrio justo entre las partes? (Ej. 1 miembro = 1 voto, voto ponderado por reputación, por contribución, etc.).
    * **Toma de Decisiones:** ¿Qué tipo de propuestas se pueden votar? (Ej. Acreditación de nuevas ONGs, actualizaciones del protocolo, asignación de fondos de la tesorería).
    * **Tesorería:** ¿Cómo se financiará la DAO (ej. una pequeña comisión por proyecto) y cómo decidirá usar sus fondos para el mantenimiento y crecimiento del ecosistema?
* **Importancia:** La DAO es lo que garantiza la descentralización, la resiliencia y la alineación a largo plazo de todos los participantes.

**Bounty 6: Privacidad y Soberanía de Datos.**
* **Misión:** Investigar y proponer un modelo para proteger la privacidad de los datos de los beneficiarios, utilizando tecnologías como ZK-Proofs, y planificar cómo un productor podría eventualmente "reclamar" la custodia de su identidad digital si en el futuro adquiere los medios para hacerlo.
* **Importancia:** Es fundamental para el cumplimiento normativo y el respeto a los derechos digitales de los beneficiarios.

---

## 5. Recursos y Apoyo

* **Documentación Original:** (https://drive.google.com/drive/folders/16r_XB9_raOtDgPoWJEm3QNomtTQXlydk?usp=sharing)
* **Diagramas de Flujo:** [Link a las imágenes PNG]
* **Equipo de Apoyo:** Estaremos disponibles en (https://discord.gg/kFJwfrjBZ) para resolver dudas.
* **Nodos y APIs:** Proveeremos acceso a un nodo de testnet de Astar/Moonbase.
