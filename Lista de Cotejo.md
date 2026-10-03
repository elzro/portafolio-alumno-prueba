# 📊 Lista de Cotejo: Evaluación Etapa 1 – Segmentación del Campus
**Asignatura:** Conectividad de Redes (CCNA 2)  
**Unidad de Evaluación:** Bloque 1 (Módulos 1-4)  
**Puntaje Máximo:** 100 Puntos  

---

## 🛑 Sección A: Filtros de Control y Políticas Obligatorias (Aceptación/Rechazo)
*Nota: Si el alumno no cumple con alguno de estos tres puntos, la práctica se penaliza automáticamente o se invalida su revisión.*

| # | Indicador de Control Técnico y Académico | Cumple (Sí) | No Cumple (No) | Observaciones / Penalización |
| :-: | :--- | :-: | :-: | :--- |
| **1** | **Filtro Anti-IA (Cronología):** El historial de GitHub del alumno muestra un **mínimo de 3 commits** realizados en días u horas diferentes durante el periodo de la práctica. | ☐ | ☐ | **Sin commits constantes: -30 puntos** sobre la nota final. |
| **2** | **Firma de Identidad CLI:** El `hostname` de los switches y el router incluye las iniciales del alumno (ej. `SW-Core-EL`). | ☐ | ☐ | **Sin firma de Hostname: No se evalúa** la sección técnica hasta corregir. |
| **3** | **Enlace Público Operativo:** El alumno configuró correctamente *GitHub Pages* y el portafolio se visualiza de forma pública a través de su URL web (`.github.io`). | ☐ | ☐ | **Enlace roto o repositorio privado: Evaluación igual a 0** hasta que sea público. |

---

## 📝 Sección B: Ponderación de Criterios Técnicos (100 Puntos Totales)

### 📊 1. Matriz de Direccionamiento e Infraestructura Digital (30 Puntos)

| # | Criterio de Evaluación | Puntos | Sí | No | Observaciones |
| :-: | :--- | :-: | :-: | :-: | :--- |
| **1.1** | **Evidencia 1 (Tablas completas):** Las celdas de la Tabla A (Dispositivos Intermedios) y Tabla B (Dispositivos Finales) fueron correctamente calculadas, sustituyendo los marcadores `[ ]` por formatos decimales y CIDR exactos. | **15** | ☐ | ☐ | |
| **1.2** | **Estructura del Portafolio:** El archivo `README.md` incluye el diagrama visual de texto de la red y está correctamente estructurado, limpio y sin faltas de ortografía. | **5** | ☐ | ☐ | |
| **1.3** | **Disponibilidad de Archivos:** El archivo de simulación `.pkt` está arriba en el repositorio principal y se puede descargar de forma directa mediante el enlace del portafolio. | **10** | ☐ | ☐ | |

### 🛠️ 2. Configuración y Funcionamiento en Packet Tracer (50 Puntos)

| # | Criterio de Evaluación | Puntos | Sí | No | Observaciones |
| :-: | :--- | :-: | :-: | :-: | :--- |
| **2.1** | **Segmentación de VLANs:** Las VLANs 10, 20, 30 y 99 se encuentran creadas en el `SW-Core`, `SW-Lab1` y `SW-Lab2` con sus nombres correspondientes y los puertos de acceso asignados según la tabla de conectividad. | **15** | ☐ | ☐ | Verificación con `show vlan brief`. |
| **2.2** | **Enlaces Troncales:** Los puertos que interconectan a los switches entre sí (`SW-Core`, `SW-Lab1`, `SW-Lab2`) y hacia el router están configurados en modo troncal con la **VLAN 99 fijada como Nativa**. | **15** | ☐ | ☐ | Verificación con `show interfaces trunk`. |
| **2.3** | **Router-on-a-Stick:** El router `R1-Core` tiene levantadas las subinterfaces encapsuladas bajo el estándar 802.1Q (`dot1Q`) para cada una de las VLANs, asignando las IP correspondientes de forma correcta. | **10** | ☐ | ☐ | Verificación con `show ip interface brief`. |
| **2.4** | **Conectividad Extremo a Extremo:** Al abrir el archivo de Packet Tracer, las PCs de diferentes VLANs (ej. Administrativos a Alumnos) logran comunicarse de forma exitosa mediante tráfico ICMP (*Ping*). | **10** | ☐ | ☐ | Pruebas de conectividad directas. |

### 🧠 3. Reporte Técnico y Reflexión Crítica (20 Puntos)

| # | Criterio de Evaluación | Puntos | Sí | No | Observaciones |
| :-: | :--- | :-: | :-: | :-: | :--- |
| **3.1** | **Firma del Captura Técnica:** Las capturas de pantalla de la CLI (`show ip route` y `show vlan brief`) muestran de forma legible la consola con el comando de verificación `show version` que evidencia el tiempo de simulación real. | **10** | ☐ | ☐ | |
| **3.2** | **Diario de Aprendizaje (Troubleshooting):** El alumno respondió las preguntas de reflexión y documentó de forma clara y honesta al menos **dos errores reales** sufridos durante la práctica, explicando su respectiva solución técnica. | **10** | ☐ | ☐ | Respuestas vacías o genéricas de IA anulan este puntaje. |

---

### 🧮 Tabla de Calificación Final
*   **Puntaje Técnico Obtenido (Sección B):** ______ / 100 Puntos.  
*   **Penalizaciones Aplicadas (Sección A):** ______ Puntos.  
*   **CALIFICACIÓN TOTAL FINAL:** ______ / 100  
