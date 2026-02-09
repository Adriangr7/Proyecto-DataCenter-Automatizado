# Diseño de Red y Direccionamiento

Esta sección documenta los parámetros de red utilizados en el tejido del
centro de datos **en el estado actual del despliegue**.

Es importante destacar que **ninguno de estos valores ha sido configurado
de forma estática o manual en los dispositivos**.  
Todas las direcciones IP, ASNs, VLANs y VNIs mostrados en este documento
han sido **definidos previamente en NetBox** y **asignados dinámicamente
por Ansible** durante el proceso de automatización.

Este documento refleja, por tanto, el **resultado del proceso de
aprovisionamiento automático**, no una configuración fija.

---

## Asignación de ASN

Los Sistemas Autónomos (ASN) se definen en NetBox y se asignan a cada
dispositivo según su rol dentro de la arquitectura.

| Rol del Dispositivo | ASN |
|--------------------|-----|
| Spine              | 65000 |
| Leaf 1             | 65101 |
| Leaf 2             | 65102 |

Estos ASNs son consumidos por Ansible desde NetBox para generar la
configuración BGP de cada nodo.

---

## Direcciones Loopback

Las direcciones loopback se definen en NetBox como direcciones lógicas
asociadas a cada dispositivo y se utilizan como identificadores
principales dentro del tejido.

| Dispositivo | Loopback0 |
|------------|-----------|
| Spine      | 172.16.0.0/32 |
| Leaf 1     | 172.16.1.0/32 |
| Leaf 2     | 172.16.1.1/32 |

Las interfaces loopback se utilizan como:
- Router-ID de BGP
- Interfaz origen del VTEP VXLAN

---

## Enlaces Underlay

Los enlaces underlay se implementan como enlaces punto a punto de Capa 3.
Las direcciones IP se asignan desde prefijos definidos en NetBox y
Ansible selecciona automáticamente las direcciones correspondientes
a cada interfaz.

| Enlace | Dirección IP |
|------|--------------|
| Spine ↔ Leaf1 | 10.0.1.138/31 – 10.0.1.139/31 |
| Spine ↔ Leaf2 | 10.0.1.140/31 – 10.0.1.141/31 |

No existe configuración manual de direccionamiento en los dispositivos.

---

## VLANs y VNIs

Las VLANs y sus correspondientes VNIs se definen en NetBox y se asocian
a los dispositivos leaf mediante automatización.

| VLAN | VNI | Propósito | Estado |
|----|----|-----------|--------|
| 10 | 1010 | Red de servidores | En uso |
| 20 | 1020 | Reservada | No usada |
| 30 | 1030 | Reservada | No usada |

Los VNIs siguen una convención de diseño:
VNI = 1000 + ID de VLAN

Aunque el escenario actual utiliza únicamente la VLAN 10, las VLANs 20
y 30 se encuentran predefinidas para facilitar la escalabilidad futura.

---

## Red de Gestión

La red de gestión está completamente separada del tráfico del data center
y se utiliza exclusivamente para operaciones de control.

| Red | Propósito |
|----|-----------|
| 192.168.18.0/24 | Gestión, automatización y acceso a Internet |

Esta red es utilizada por:
- Ansible
- NetBox
- Acceso administrativo
- Monitorización y observabilidad
