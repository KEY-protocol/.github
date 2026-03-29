# KEY Protocol 🗝️

**Infraestructura de Verificación Confidencial para el Impacto Global.**

KEY Protocol es una infraestructura de software diseñada para transformar la validación de impacto mediante la transparencia colaborativa. Resolvemos el dilema entre Transparencia vs. Privacidad mediante una arquitectura que permite ejecutar agentes de IA en entornos de computación confidencial. Esto facilita la validación de identidades y evidencias territoriales on-chain sin que los datos sensibles de los registros sean expuestos o utilizados para fines externos.

**🌐 Website:** https://keyprotocol.ar


## 🚀 Misión

El sector de impacto y la trazabilidad de activos reales mueven billones de dólares pero operan sobre infraestructura obsoleta. KEY Protocol permite tokenizar activos reales (RWA) —como hectáreas regeneradas, cumplimiento de normas corporativas o hitos sociales— mediante una arquitectura de verificación confidencial y Offline-First, conectando la liquidez global con la ejecución local.


## 🏗️ Arquitectura Técnica (MVP Fase 1)

KEY Protocol opera mediante una red federada de Nodos Soberanos, permitiendo que cada organización (ONG, Empresa o Institución) mantenga el control total de sus datos operativos:

**📱 Capa de Cliente (Field App)**

* **Tecnología:** React Native (Expo).
 
* **Captura Territorial:** Registro de activos, evidencias fotográficas, geolocalización y biometría en modo Offline-First.

* **Cifrado en el Origen:** Los datos se encriptan localmente en el dispositivo. 

Nada se almacena en texto plano, garantizando la seguridad en caso de pérdida del equipo.


## 🆔 Motor de Identidad Nativo

* **Vectorizado por IA Propio:** Implementamos un sistema interno que convierte datos biométricos ruidosos en vectores criptográficos estables.

* **Soberanía:** La identidad se genera y valida en el perímetro del Nodo; no dependemos de protocolos de identidad externos para el MVP, asegurando la propiedad intelectual y la privacidad absoluta.


## ⛓️ Capa de Consenso (Astar Network)

* **Smart Contracts:** Desarrollados en Solidity.

* **Red:** Desplegados en Astar Network (EVM), aprovechando la escalabilidad del ecosistema Polkadot.

* **Anclaje Inmutable:** Registramos exclusivamente el Hash de Identidad + CID, creando una prueba de impacto auditable públicamente sin revelar el contenido sensible.


## 🔒 Almacenamiento & Oráculo de Privacidad

* **IPFS:** Almacenamiento descentralizado para los paquetes de evidencia cifrados.

* **Servidor Intermedio (TEE Emulator):** Backend en Python que emula un entorno seguro para el procesamiento de IA (Google Vertex AI). Actúa como relayer de gas, eliminando la barrera técnica de gestionar billeteras cripto en el territorio.


## 🛠️ Stack Tecnológico

Componente

Tecnología

Frontend

React, Vite, TailwindCSS

Smart Contracts

Solidity, Hardhat, Ethers.js

Blockchain

Astar Network (EVM)

Backend / Scripting

Python (Fuzzy Extractor, API Gateway)

Storage

IPFS (Pinata)


## 📂 Estructura del Repositorio

key-protocol/

├── contracts/______# Smart Contracts (Solidity)

├── frontend/_______# Web App (React/Vite)

├── scripts/_________# Scripts de despliegue y utilidades Python

├── docs/___________# Documentación técnica y Whitepaper

└── README.md____# Este archivo


## 🏁 Roadmap (MVP)

[x] Diseño de Arquitectura sobre Astar EVM.

[x] Desarrollo de la Field App (Captura Offline).

[x] Implementación del Motor de Vectorizado IA Propio.

[ ] Integración de Cifrado Asimétrico para Nodos.

[ ] Despliegue de contratos en blockchain.

[ ] Piloto territorial con Nodos en el Gran Chaco (5 ONGs).


## 🤝 Contribuir

**¡Las contribuciones son bienvenidas!** Si eres desarrollador o formas parte de una organización:

* Haz un Fork del proyecto.

* Crea tu rama de funcionalidad (git checkout -b feature/AmazingFeature).

* Haz Commit de tus cambios.

* Abre un Pull Request.


## 📞 Contacto & Comunidad
¿Tienes dudas técnicas o quieres integrar tu ONG?

📧 Email Desarrolladores: developers@keyprotocol.ar

🐦 Twitter/X: @key_protocol

🌍 Website: keyprotocol.ar

<br />
<p align="center">
<sub>Desarrollado con ❤️ en el Gran Chaco Argentino by KEY protocol. Powered by Fundacion Gran Chaco, UTN, Latin Hack & NERDCONF.</sub>
</p>
