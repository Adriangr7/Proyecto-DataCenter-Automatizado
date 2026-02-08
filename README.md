# Automated Data Center Fabric with VXLAN EVPN
## Spine–Leaf Architecture | BGP | Ansible | NetBox | Kubernetes

[🇪🇸 Español](#-descripción-general) | [🇬🇧 English](#-overview)

---

## 🔹 Descripción General 🇪🇸

Este proyecto implementa un **Data Center moderno completamente automatizado**
basado en una **topología Spine–Leaf**, utilizando **BGP como underlay** y
**VXLAN EVPN como overlay**.

La automatización se realiza mediante **Ansible**, consumiendo la información
definida en **NetBox como Source of Truth**, permitiendo una configuración
**data-driven, reproducible y escalable**.

Los servidores ejecutan **Docker y Kubernetes**, simulando un entorno real
donde los servicios se despliegan de forma homogénea en múltiples nodos.

El proyecto ha sido desarrollado íntegramente sobre **máquinas virtuales Ubuntu**
y **Arista vEOS**, simulando un entorno de Data Center real.

---

## 🔹 Tecnologías utilizadas

- Spine–Leaf Architecture
- BGP (Underlay)
- VXLAN EVPN (Overlay)
- Arista vEOS
- Ansible (Network Automation)
- NetBox (Source of Truth)
- Docker & Kubernetes
- Ubuntu Server
- Git & GitHub

---

## 🔹 Objetivos del proyecto

- Diseñar una arquitectura de Data Center moderna
- Implementar VXLAN EVPN con BGP
- Automatizar completamente la red usando Ansible
- Usar NetBox como fuente única de verdad
- Separar red de gestión y red de datos
- Simular un entorno real de producción

---

## 🔹 Documentación

- 📘 [Arquitectura](docs/es/02-arquitectura.md)
- 📘 [NetBox como Source of Truth](docs/es/04-netbox.md)
- 📘 [Underlay BGP](docs/es/05-underlay-bgp.md)
- 📘 [Overlay VXLAN EVPN](docs/es/06-overlay-vxlan-evpn.md)
- 📘 [Automatización con Ansible](docs/es/07-ansible.md)
- 📘 [Validación y pruebas](docs/es/09-validacion.md)

---

---

## 🔹 Overview 🇬🇧

This project implements a **fully automated modern Data Center**
based on a **Spine–Leaf architecture**, using **BGP as underlay** and
**VXLAN EVPN as overlay**.

Network automation is achieved using **Ansible**, consuming data
defined in **NetBox as the Source of Truth**, enabling a **data-driven,
scalable and reproducible** workflow.

Servers run **Docker and Kubernetes**, simulating a real production
environment where services are deployed consistently across nodes.

The entire project is built using **Ubuntu virtual machines** and
**Arista vEOS**, closely emulating a real-world data center fabric.

---

## 🔹 Technologies

- Spine–Leaf Architecture
- BGP Underlay
- VXLAN EVPN Overlay
- Arista vEOS
- Ansible Network Automation
- NetBox (Source of Truth)
- Docker & Kubernetes
- Ubuntu Server

---

## 🔹 Project Goals

- Design a modern data center fabric
- Implement VXLAN EVPN with BGP
- Achieve full network automation using Ansible
- Use NetBox as a centralized Source of Truth
- Separate management and data networks
- Simulate real-world production scenarios

---

## 🔹 Documentation

- 📘 [Architecture](docs/en/02-architecture.md)
- 📘 [NetBox as Source of Truth](docs/en/04-netbox.md)
- 📘 [BGP Underlay](docs/en/05-underlay-bgp.md)
- 📘 [VXLAN EVPN Overlay](docs/en/06-overlay-vxlan-evpn.md)
- 📘 [Automation with Ansible](docs/en/07-ansible.md)
- 📘 [Validation & Testing](docs/en/09-validation.md)
