# 🧩 Proyecto de Redes I – Contabiliza S.A.  
**Configuración de Servidor DHCP, DNS e Infraestructura de Red Empresarial Segmentada**

---

## 📘 Descripción General
Este proyecto tiene como objetivo la **modernización completa de la infraestructura de red** de la empresa contable **Contabiliza S.A.**, mediante la **implementación de servicios de red internos** y la **segmentación lógica por VLANs**.  
El diseño fue desarrollado como parte del curso **Redes I (BIS-13)** en la **Universidad Latina de Costa Rica**, aplicando estándares y metodologías reales de ingeniería de redes.

El trabajo abarca la **configuración de un servidor DHCP y DNS**, la **integración de un servidor de correo interno**, una **intranet corporativa**, y la **implementación de un cableado estructurado** basado en **categoría 6** y puntos de acceso inalámbricos **Wi-Fi 6**, todo validado mediante simulación en **Cisco Packet Tracer**.

---

## 🎯 Objetivos del Proyecto

- Automatizar la asignación de direcciones IP mediante un **servidor DHCP centralizado**.  
- Implementar un **servidor DNS interno** para la resolución de nombres locales.  
- Segmentar la red mediante **VLANs** para cada departamento (Administración, Ventas, Soporte Técnico, Almacén y Servicios).  
- Integrar servicios internos: **correo electrónico (SMTP/IMAP)** e **intranet web corporativa**.  
- Mejorar la **seguridad, rendimiento y escalabilidad** de la red de la empresa.  
- Cumplir con **estándares de cableado y protocolos IEEE** vigentes.

---

## 🏗️ Arquitectura General del Sistema de Red

El diseño se basa en una **arquitectura jerárquica empresarial**:

### 🔹 Capa de Acceso
- Switches gestionables con VLANs (Administración, Ventas, Soporte, Almacén, Servicios).  
- Cableado estructurado **Cat 6** según norma **TIA/EIA-568**.  
- Integración de puntos de acceso inalámbricos **Wi-Fi 6 (802.11ax)**.

### 🔹 Capa de Distribución
- Routers con **enrutamiento inter-VLAN** y **subneteo VLSM** optimizado.  
- Configuración de políticas de acceso y direccionamiento interno por departamento.  

### 🔹 Capa de Núcleo / Servidores
- **Servidor DHCP:** Asignación dinámica de IPs segmentada por VLAN.  
- **Servidor DNS:** Resolución de nombres internos (ej. `intranet.contabiliza.local`).  
- **Servidor Web:** Intranet corporativa para noticias, documentos y recursos internos.  
- **Servidor de Correo:** SMTP/IMAP bajo dominio interno (`@contabiliza.local`).  

---

## ⚙️ Tecnologías y Herramientas

| Categoría | Tecnologías |
|------------|-------------|
| **Simulación** | Cisco Packet Tracer |
| **Protocolos de Red** | VLANs, DHCP, DNS, SMTP/IMAP, HTTP, ICMP |
| **Hardware (simulado)** | Routers TP-Link BE19000, Switches Gigabit administrables, Access Points Wi-Fi 6 |
| **Cableado** | Categoría 6 (TIA-568), Patch Panels, RJ45 |
| **Sistemas Operativos** | Windows Server 2022, Ubuntu Server |
| **Servicios Implementados** | DHCP, DNS, Mail Server, Web Server (Intranet) |
| **Estándares aplicados** | IEEE 802.3, IEEE 802.11ax, ISO/IEC 27001, TIA-568 |

---

## 🧮 Plan de Direccionamiento IP

| Departamento | VLAN | Subred | Rango de IPs | Gateway |
|---------------|------|---------|--------------|----------|
| Administración | 10 | 192.168.10.0/26 | .1–.62 | 192.168.10.1 |
| Ventas | 20 | 192.168.20.0/25 | .1–.126 | 192.168.20.1 |
| Soporte Técnico | 30 | 192.168.30.0/27 | .1–.30 | 192.168.30.1 |
| Almacén | 40 | 192.168.40.0/28 | .1–.14 | 192.168.40.1 |
| Servicios | 50 | 192.168.50.0/28 | .1–.14 | 192.168.50.1 |

---

## 🔐 Seguridad y Buenas Prácticas

- Segmentación por VLANs para aislar tráfico entre departamentos.  
- Contraseñas seguras y acceso restringido por roles (consola, VTY).  
- Políticas de firewall y ACLs para controlar acceso entre VLANs.  
- Servidores internos protegidos y autenticados dentro de red local.  
- Cableado estructurado bajo normativa TIA/EIA-568 para minimizar interferencias.  
- Control de tráfico y priorización mediante QoS y administración centralizada.  

---

## 🧪 Pruebas de Validación

✅ **DHCP:** Asignación automática de IPs por VLAN.  
✅ **DNS:** Resolución correcta de dominios internos.  
✅ **Correo interno:** Envío y recepción local mediante SMTP/IMAP.  
✅ **Intranet:** Acceso web interno desde todos los departamentos.  
✅ **Wi-Fi:** Conectividad estable bajo WPA3 y VLAN asignada.  
✅ **Simulación:** Conectividad validada en Cisco Packet Tracer sin pérdida de paquetes.  

---

## 📈 Resultados Principales

- Eliminación de conflictos de IP y reducción del 100% en configuraciones manuales.  
- Mejora del rendimiento de red y segregación del tráfico interno.  
- Red inalámbrica estable y segura con cobertura total.  
- Integración exitosa de servicios internos (DNS, correo, intranet).  
- Escalabilidad para futuras expansiones sin rediseño completo.  

---

## 💡 Recomendaciones Futuras

- Implementar redundancia en servidores (clúster DHCP/DNS).  
- Agregar **monitorización en tiempo real (SNMP/Nagios)**.  
- Aplicar políticas avanzadas de seguridad (IDS/IPS, segmentación adicional).  
- Migrar servicios críticos a infraestructura híbrida (on-premise + nube).  
- Documentar mantenimiento preventivo y plan de expansión.  

---

## 🧑‍💻 Autores

- **Santiago Ramírez Elizondo**  
- **Jonatan Fabricio Grande López**

Profesor: *Bryan Vega Rondón*  
Curso: *Redes I – Universidad Latina de Costa Rica*  
Fecha: *Febrero 2025*

---

## 📎 Archivos Incluidos

- 🗂️ `ProyectoContabilizaSA_Redes1.pkt` → Topología en Cisco Packet Tracer  
- 📄 `Documentación Técnica.pdf` → Detalles de configuración, VLANs, DHCP/DNS  
- 🧾 `README.md` → Este documento  

---

## 🏁 Licencia
Proyecto académico para fines educativos.  
Puedes utilizar este contenido como referencia citando a los autores y la institución.

---
