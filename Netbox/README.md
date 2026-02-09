# NetBox – Fuente de la Verdad

NetBox se utiliza como la fuente única de verdad para toda la infraestructura.

## Objetos Gestionados
- Dispositivos (Spine, Leaf, Servidores)
- Interfaces
- Direcciones IP
- Prefijos
- ASNs
- VLANs
- VNIs

## Flujo de Automatización
1. Los datos de infraestructura se definen en NetBox
2. Ansible obtiene los datos mediante la API de NetBox
3. Los playbooks generan configuraciones dinámicamente
4. Los dispositivos se configuran de forma automática

## Beneficios
- Sin valores hardcodeados en Ansible
- Consistencia en direccionamiento y configuración
- Escalabilidad sencilla
- Flujo de trabajo NetDevOps realista
