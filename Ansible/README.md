# Automatización con Ansible

Ansible se utiliza para automatizar completamente la configuración del
DATA CENTER.

## Componentes Automatizados
- Configuración de spine y leaf
- Underlay BGP
- Overlay VXLAN EVPN
- Mapeo VLAN/VNI
- Configuración del gateway anycast

## Fuentes de Datos
- NetBox (inventario dinámico)
- Variables de grupo y host generadas desde NetBox

## Principios de Automatización
- Playbooks idempotentes
- Sin configuración manual en dispositivos
- Plantillas generadas mediante Jinja2
