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

| Dispositivo / Interfaz | VLAN Asociada | Dirección IP | Máscara de Subred | Gateway por Defecto |
| :--- | :---: | :--- | :--- | :--- |
| **R1-Core** (`G0/0/0.10`) | 10 (Admin) | `192.168.10.254` | `255.255.255.0` | N/A |
| **R1-Core** (`G0/0/0.20`) | 20 (Alumnos) | `192.168.20.254` | `255.255.255.0` | N/A |
| **R1-Core** (`G0/0/0.30`) | 30 (Dirección) | `192.168.30.254` | `255.255.255.0` | N/A |
| **R1-Core** (`G0/0/0.99`) | 99 (Gestión) | `192.168.99.254` | `255.255.255.0` | N/A |
| **SW-Core** (`VLAN 99`) | 99 (Gestión) | `192.168.99.1` | `255.255.255.0` | `192.168.99.254` |
| **SW-Lab1** (`VLAN 99`) | 99 (Gestión) | `192.168.99.2` | `255.255.255.0` | `192.168.99.254` |
| **SW-Lab2** (`VLAN 99`) | 99 (Gestión) | `192.168.99.3` | `255.255.255.0` | `192.168.99.254` |

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

