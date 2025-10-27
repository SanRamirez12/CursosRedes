# 🧩 Proyecto Final – Redes II  
**Diseño e Implementación de una Infraestructura de Red Segmentada con VLANs, Servicios Integrados y Ciberseguridad Básica**

---

## 📘 Descripción General
Este proyecto presenta el diseño y la implementación de una **infraestructura de red segmentada** para la empresa ficticia **NexaCapital S.A.**, dedicada a servicios financieros y de inversión.  
El objetivo fue construir una red **escalable, segura y funcional** bajo un entorno multidepartamental, integrando servicios esenciales como **DNS, DHCP, correo corporativo, intranet HTTP**, y mecanismos básicos de **ciberseguridad** mediante **ACLs** y segmentación por **VLANs**.

---

## 🎯 Objetivos Principales

- **Diseñar una red jerárquica** bajo el modelo de capas (Acceso – Distribución – Núcleo).  
- **Segmentar la red** mediante VLANs para mejorar seguridad y rendimiento.  
- **Automatizar servicios de red** con DNS, DHCP y correo interno.  
- **Implementar protocolos de enrutamiento dinámico** (OSPF y BGP) para garantizar conectividad interna y externa.  
- **Aplicar medidas de seguridad básicas**, como ACLs, contraseñas seguras y protección de puertos.  
- **Cumplir con normativas internacionales** como ISO 27001 y la Ley 8968 de Protección de Datos Personales (Costa Rica).

---

## 🏗️ Arquitectura General

**Topología jerárquica de red:**
- **Capa de acceso:** Switches gestionables con VLANs 10 (Finanzas), 20 (RRHH), 30 (Administración) y 40 (TI).  
- **Capa de distribución:** Routers intermedios con configuración *router-on-a-stick* y OSPF.  
- **Capa núcleo:** Router principal con conexión a ISP y sesión BGP establecida para intercambio de rutas.

**Servicios integrados:**
- **DNS:** Resolución interna de nombres (Bind / Windows Server).  
- **DHCP:** Asignación dinámica de direcciones IP por VLAN.  
- **HTTP:** Intranet corporativa accesible desde todos los departamentos.  
- **Correo corporativo:** SMTP / POP3 configurados para comunicación interna.  
- **ACLs:** Control de tráfico entre departamentos para segmentación lógica y seguridad.

---

## 🧰 Tecnologías Utilizadas

| Categoría | Tecnologías |
|------------|-------------|
| **Simulación** | Cisco Packet Tracer |
| **Protocolos** | VLANs, OSPF, BGP, DHCP, DNS, SMTP/POP3, HTTP |
| **Seguridad** | ACLs, Port-Security, Password Encryption, BPDU Guard |
| **Estándares aplicados** | IEEE 802.1Q, 802.11ax, ISO/IEC 27001, TIA-568, Ley 8968 |
| **Hardware simulado** | Routers, switches, servidores, PCs, puntos de acceso |

---

## 🧮 Plan de Direccionamiento IP

| Departamento | VLAN | Subred | Rango de IPs | Gateway |
|---------------|------|---------|--------------|----------|
| Finanzas | 10 | 192.168.0.0/25 | .0 – .127 | 192.168.0.1 |
| RRHH | 20 | 192.168.0.128/26 | .128 – .191 | 192.168.0.129 |
| Administración | 30 | 192.168.0.192/26 | .192 – .255 | 192.168.0.193 |
| TI | 40 | 192.168.1.0/27 | .0 – .31 | 192.168.1.1 |

Enlaces seriales /30 entre routers y conexión ISP con BGP (red 10.0.0.0/30).

---

## 🔐 Medidas de Seguridad

- Configuración de **ACLs** para limitar el tráfico inter-VLAN.  
- **Contraseñas cifradas** y autenticación en consola y VTY.  
- **Port-Security** y **BPDU Guard** en switches de acceso.  
- Políticas de **contraseña segura y control de acceso**.  
- Segmentación y aislamiento de tráfico sensible por departamento.  

---

## 🧪 Pruebas Realizadas

- **Conectividad interna:** Ping exitoso entre VLANs vía OSPF.  
- **DHCP/DNS:** Asignación automática de IPs y resolución correcta de dominios internos.  
- **HTTP:** Intranet corporativa funcional desde todos los departamentos.  
- **Correo electrónico:** SMTP funcional; pruebas POP3 parcialmente exitosas (ajuste en servidor).  
- **BGP:** Sesión establecida con ISP (pendiente redistribución NAT para ping externo).  
- **Seguridad:** Sin violaciones en port-security; ACLs planificadas y probadas.

---

## 📈 Resultados y Aprendizajes

- Lograda **conectividad total** entre departamentos y funcionamiento correcto de servicios DNS/DHCP.  
- Establecida **sesión BGP** con ISP y OSPF entre routers internos.  
- **Segmentación VLAN exitosa** y tráfico controlado entre áreas.  
- Identificados puntos de mejora: redistribución BGP→OSPF y configuración POP3.  
- Se aplicaron buenas prácticas de documentación, nomenclatura y estandarización.

---

## 💡 Recomendaciones Técnicas

- Implementar **SSH**, **AAA** y **autenticación OSPF** para reforzar seguridad.  
- Agregar **HSRP/VRRP** y **EtherChannel** para alta disponibilidad.  
- Incluir **DHCP Snooping**, **DAI** y **QoS** para voz/datos.  
- Documentar configuraciones y mantener respaldos automáticos.  
- Preparar migración gradual a **infraestructura híbrida (on-premise + nube)**.

---

## 🧑‍💻 Autores

- **Santiago Ramírez Elizondo**  
- **David Abarca Chaves**  
- **Alberto Álvarez Navarro**  
- **Sebastián Chaves Solano**

Profesor: *Daniel Adolfo Ramírez González*  
Curso: *BTI-13 Redes II – Universidad Latina de Costa Rica*  
Fecha: *Mayo 2025*

---


## 🏁 Licencia
Este proyecto se desarrolló con fines educativos bajo el curso **Redes II**.  
Puedes usarlo como referencia académica citando a los autores.

