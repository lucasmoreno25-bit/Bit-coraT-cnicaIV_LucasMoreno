# 

# 

# 

# El Marco Legal y la Estructura del "Relato"

Nombre:Lucas Moreno Bravo  
Módulo:Desarrollo de Aplicaciones Multiplataformas  
Fecha:15/05/2026

**Indice**

1.[Problemáticas de negocio resueltas por la solución](#id1)
1.1 [Centralización y homogeneidad del acceso:](#id1.1)
1.2 [Con la implementación de Ahorro drástico de recursos (Eficiencia Operativa)](#id1.2)
2.[Razones de la exclusión de conexiones directas por RDP a cada máquina ](#id2)
2.1 [Superficie de ataque crítica:](#id2.1)
2.2 [Dependencias y fragmentación en el cliente final:](#id2.2)

# Introducción {#introducción}

Con el objetivo de optimizar la infraestructura tecnológica de la organización y dar respuesta a las necesidades actuales de movilidad, eficiencia y gobernanza del dato, se presenta a continuación la justificación técnica de la solución implantada basada en Apache Guacamole orquestado sobre contenedores Docker, en contraste con los modelos tradicionales de conexión remota.

# 1\. Problemáticas de negocio resueltas por la solución <a name="id1"></a>

Esta arquitectura resuelve de manera directa tres de los dolores más críticos en la gestión de TI y la continuidad de negocio:

## **Centralización y homogeneidad del acceso:**  <a name="id1.1"></a>

Anteriormente, el soporte y la entrega de herramientas a los usuarios dependían de complejas configuraciones locales, clientes pesados y la gestión individual de conexiones VPN.

## **Con la implementación de Ahorro drástico de recursos (Eficiencia Operativa):**  <a name="id1.2"></a>

Al empaquetar los entornos de escritorio y las aplicaciones dentro de contenedores Docker (como linuxserver/webtop), se elimina la necesidad de aprovisionar máquinas virtuales (VM) completas con hipervisores tradicionales para cada puesto de trabajo.

# 2\. Razones de la exclusión de conexiones directas por RDP a cada máquina <a name="id2"></a>

La opción de exponer o conectar directamente mediante el protocolo RDP (Remote Desktop Protocol) a cada estación de trabajo individual se descartó por considerarse una práctica de alto riesgo e ineficiente en la ingeniería de sistemas moderna:

## **Superficie de ataque crítica:**  <a name="id2.1"></a>

El protocolo RDP es uno de los vectores más explotados por los ciberdelincuentes debido a sus vulnerabilidades de seguridad históricas. Exponer múltiples puertos RDP a internet para cada empleado exigiría una gestión de cortafuegos insostenible o forzaría el uso obligatorio de una VPN.

## 

## **Dependencias y fragmentación en el cliente final:**  <a name="id2.2"></a>

El acceso RDP nativo requiere clientes de escritorio específicos cuya experiencia y rendimiento varían sustancialmente entre sistemas operativos (macOS, Linux, Android, iOS), multiplicando los incidentes de soporte técnico.

