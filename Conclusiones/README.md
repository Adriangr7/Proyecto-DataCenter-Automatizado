🧾 CONCLUSIÓN

En este proyecto se ha diseñado e implementado con éxito un DATA CENTER moderno basado en una arquitectura Spine–Leaf, utilizando BGP como protocolo de enrutamiento en el plano underlay y VXLAN EVPN como tecnología de overlay para proporcionar conectividad de capa 2 sobre una infraestructura de capa 3.

Uno de los aspectos fundamentales del trabajo ha sido la automatización completa de la infraestructura, apoyándose en NetBox como Source of Truth. Todas las direcciones IP, VLANs, VNIs, ASN y parámetros de red han sido definidos de forma centralizada, permitiendo que Ansible genere y aplique las configuraciones de manera dinámica y consistente, eliminando la necesidad de configuraciones manuales y reduciendo el riesgo de errores humanos.

La separación de planos —gestión, control y datos— ha permitido un diseño más robusto y escalable, alineado con las mejores prácticas actuales en centros de datos. La red de gestión independiente facilita tanto el acceso administrativo como los procesos de automatización y monitorización, sin interferir con el tráfico del plano de datos.

Sobre esta infraestructura de red se ha desplegado una plataforma de contenedores basada en Kubernetes (k3s), demostrando la correcta integración entre la red VXLAN EVPN del centro de datos y el plano de red del clúster. Los servicios desplegados (Nginx, Redis y Prometheus) se distribuyen entre los nodos, validando la conectividad extremo a extremo y la alta disponibilidad básica del sistema.

Las validaciones realizadas mediante comandos de control, así como las capturas de tráfico, confirman el correcto funcionamiento de los distintos componentes: establecimiento de sesiones BGP, intercambio de rutas EVPN, descubrimiento de VTEPs y encapsulación VXLAN del tráfico entre servidores. Estos resultados demuestran que la solución implementada es funcional, coherente y representativa de un entorno real de producción.

En conjunto, el proyecto cumple los objetivos planteados y sirve como una base sólida para comprender y aplicar conceptos avanzados de redes de centros de datos, automatización y plataformas de contenedores, situándose en línea con los enfoques actuales utilizados en entornos profesionales de NetDevOps.
