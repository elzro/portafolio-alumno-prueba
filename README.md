# 🌐 Mi Portafolio de Redes: Proyecto Campus Conalep039
**Estudiante:** Enrique Lzro  
**Matrícula/Código:** [Tu Código de Alumno]  
**Grupo:** [Tu Grupo]  
**Enlace a mi sitio web público:** [Pega aquí el enlace de tu GitHub Pages]

---

## 🏢 Presentación del Caso
Este portafolio digital documenta paso a paso la construcción de la red para el *Campus Conalep039*. A lo largo de tres unidades, se registrarán las configuraciones técnicas, códigos CLI y la solución de problemas (troubleshooting) con base en el temario oficial de Cisco CCNA 2 (SRWE v7).

---

## 📍 Etapa 1: Infraestructura Base y Segmentación (Módulos 1-4)

### 🗺️ 1. Topología Física Oficial de la Red
*Conecta los dispositivos en Cisco Packet Tracer siguiendo estrictamente este esquema de estrella extendida:*

```text
               [ R1-Core (Router) ]
                        |
                        | (Interfaz G0/0/0)
                        |
                 [ SW-Core ] ------------- Dispositivos Locales:
                  /       \                ├── VLAN 99: 1 PC Gestión
                 /         \               ├── VLAN 10: 6 PCs Administrativos
                /           \              └── VLAN 30: 2 PCs Dirección
               /             \
          [ SW-Lab1 ]    [ SW-Lab2 ]

              |                |
       (VLAN 20: 3 PCs) (VLAN 20: 3 PCs)
```

### 🛠️ 2. Archivo de Simulación
*   **Enlace de descarga:** [Descarga aquí mi archivo de Packet Tracer (.pkt)](📌 REEMPLAZAR_ESTE_TEXTO_CON_EL_ENLACE_A_TU_ARCHIVO_PKT)
*   *Nota: Recuerda que el archivo .pkt debe estar subido en este mismo repositorio de GitHub.*

### 📋 3. Tabla de Direccionamiento IP y Equipos
*Completa los datos de la red asignada de acuerdo a las configuraciones de tus subinterfaces en el Router y las SVIs de los switches:*

### 📋 3. Tablas de Direccionamiento IP y Equipos

**Instrucciones para el estudiante:** Con base en las máscaras de subred y los segmentos asignados, calcula y completa las celdas vacías utilizando las reglas y las IPs aleatorias asignadas para cada host.

#### Tabla A: Dispositivos Intermedios (Routers y Switches)

| Dispositivo / Interfaz | VLAN | Segmento de Red Base | Dirección IP a Calcular / Configurar | Máscara de Subred | Gateway por Defecto |
| :--- | :---: | :--- | :--- | :--- | :--- |
| **R1-Core** (`G0/0/0.10`) | 10 | `192.168.10.0/24` | **Última IP utilizable del segmento** | `255.255.255.0` | *No aplica* |
| **R1-Core** (`G0/0/0.20`) | 20 | `192.168.20.0/24` | **Última IP utilizable del segmento** | `255.255.255.0` | *No aplica* |
| **R1-Core** (`G0/0/0.30`) | 30 | `192.168.30.0/24` | **Última IP utilizable del segmento** | `255.255.255.0` | *No aplica* |
| **R1-Core** (`G0/0/0.99`) | 99 | `192.168.99.0/24` | **Última IP utilizable del segmento** | `255.255.255.0` | *No aplica* |
| **SW-Core** (SVI `VLAN 99`) | 99 | `192.168.99.0/24` | **1ª IP utilizable del segmento** | `255.255.255.0` | **Última IP utilizable** |
| **SW-Lab1** (SVI `VLAN 99`) | 99 | `192.168.99.0/24` | **2ª IP utilizable del segmento** | `255.255.255.0` | **Última IP utilizable** |
| **SW-Lab2** (SVI `VLAN 99`) | 99 | `192.168.99.0/24` | **3ª IP utilizable del segmento** | `255.255.255.0` | **Última IP utilizable** |

#### Tabla B: Dispositivos Finales (PCs de Usuario y Gestión)

| Dispositivo Final | VLAN | Segmento de Red Base | Dirección IP Asignada | Máscara de Subred | Gateway por Defecto |
| :--- | :---: | :--- | :--- | :--- | :--- |
| **PC-Administrativos-1** | 10 | `192.168.10.0/24` | `192.168.10.15` | `255.255.255.0` | |
| **PC-Administrativos-2** | 10 | `192.168.10.0/24` | `192.168.10.42` | `255.255.255.0` | |
| **PC-Administrativos-3** | 10 | `192.168.10.0/24` | `192.168.10.77` | `255.255.255.0` | |
| **PC-Administrativos-4** | 10 | `192.168.10.0/24` | `192.168.10.101` | `255.255.255.0` | |
| **PC-Administrativos-5** | 10 | `192.168.10.0/24` | `192.168.10.130` | `255.255.255.0` | |
| **PC-Administrativos-6** | 10 | `192.168.10.0/24` | `192.168.10.185` | `255.255.255.0` | |
| **PC-Dirección-1**       | 30 | `192.168.30.0/24` | `192.168.30.22` | `255.255.255.0` | |
| **PC-Dirección-2**       | 30 | `192.168.30.0/24` | `192.168.30.88` | `255.255.255.0` | |
| **PC-Gestión** (Única)    | 99 | `192.168.99.0/24` | `192.168.99.50` | `255.255.255.0` | |
| **PC-Alumnos-Lab1-A**    | 20 | `192.168.20.0/24` | `192.168.20.33` | `255.255.255.0` | |
| **PC-Alumnos-Lab1-B**    | 20 | `192.168.20.0/24` | `192.168.20.65` | `255.255.255.0` | |
| **PC-Alumnos-Lab1-C**    | 20 | `192.168.20.0/24` | `192.168.20.120` | `255.255.255.0` | |
| **PC-Alumnos-Lab2-A**    | 20 | `192.168.20.0/24` | `192.168.20.142` | `255.255.255.0` | |
| **PC-Alumnos-Lab2-B**    | 20 | `192.168.20.0/24` | `192.168.20.199` | `255.255.255.0` | |
| **PC-Alumnos-Lab2-C**    | 20 | `192.168.20.0/24` | `192.168.20.210` | `255.255.255.0` | |


### 📸 4. Evidencias de Verificación (CLI con Firma de Identidad)
> **Instrucciones obligatorias Anti-IA:** Pega aquí abajo las capturas de pantalla de tu CLI de Packet Tracer. Recuerda que el nombre del dispositivo debe incluir tus iniciales (ej. `SW-Core-EL`) y debes ejecutar el comando `show version` en la misma ventana de la consola para validar el tiempo de simulación activo.

*   **Evidencia 1: Demostración de VLANs creadas en el SW-Core (`show vlan brief`)**
    ![Captura VLANs SW-Core](📌 ENLACE_A_TU_CAPTURA_VLAN)

*   **Evidencia 2: Tabla de enrutamiento en el Router Core (`show ip route`)**
    ![Captura Enrutamiento Router](📌 ENLACE_A_TU_CAPTURA_ROUTE)

*   **Evidencia 3: Prueba de conectividad exitosa (Ping entre una PC de Administrativos de la VLAN 10 y una PC de Alumnos de la VLAN 20)**
    ![Captura Ping Exitoso](📌 ENLACE_A_TU_CAPTURA_PING)

### 📝 5. Diario de Aprendizaje y Troubleshooting (Anti-IA)
*   **¿Cuál fue el mayor reto técnico que enfrentaste en esta unidad?**  
    [Escribe aquí tu respuesta con tus propias palabras]

*   **Bitácora de Errores (Documenta al menos 2 fallas reales que te ocurrieron durante la práctica y cómo las solucionaste):**  
    1. **Error 1:** [Ej: Olvidé poner el comando encapsulation dot1Q en la subinterfaz .10 del Router]  
       **Solución:** [Ej: Entré a la subinterfaz, ejecuté encapsulation dot1q 10 y el tráfico comenzó a fluir de inmediato]  
    2. **Error 2:** [Escribe aquí tu segundo error o comando mal digitado]  
       **Solución:** [Escribe cómo lo solucionaste usando comandos de diagnóstico de Cisco]

---
*(Las secciones para la Etapa 2 y Etapa 3 se añadirán en este mismo archivo conforme se avance en el semestre)*

