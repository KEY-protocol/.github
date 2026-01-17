# KEY Protocol 🗝️

**Infraestructura de Verificación Confidencial para Impacto Social.**

KEY Protocol es una plataforma SaaS descentralizada que permite a las ONGs validar identidades y evidencias territoriales on-chain sin exponer datos sensibles. Conectamos la liquidez global con la ejecución local, garantizando privacidad y trazabilidad.

**🌐 Website:** https://keyprotocol.ar


## 🚀 Misión
El sector de impacto social mueve billones de dólares pero opera con herramientas obsoletas. KEY Protocol resuelve el dilema de la privacidad: ¿Cómo trazar fondos en blockchain sin vulnerar los datos de los beneficiarios?

Nuestra solución permite tokenizar activos reales (RWA) de impacto (como hectáreas protegidas o habilidades adquiridas) mediante una arquitectura de Verificación Confidencial y Offline-First.


## 🏗️ Arquitectura Técnica
KEY Protocol opera bajo una arquitectura híbrida optimizada para el Gran Chaco y escalable globalmente:

**📱 Capa de Cliente (Offline-First)**

* **Web App (PWA):** Desarrollada en React/Vite.

* **Captura Offline:** Captura de datos biométricos y evidencias en campo sin necesidad de internet.

* **Persistencia Local:** Almacenamiento local seguro (IndexedDB) hasta la sincronización.


## 🆔 Motor de Identidad Nativa

* **Fuzzy Extractors:** Implementación propia (Python/WASM) para generar identificadores criptográficos estables a partir de biometría ruidosa.

* **Soberanía:** No dependemos de terceros; la identidad es soberana y generada en el dispositivo.


## ⛓️ Capa de Consenso (Astar Network)
Smart Contracts: Escritos en Solidity.

* **Red:** Desplegados en Astar Network (Shibuya Testnet / Astar Mainnet) aprovechando su compatibilidad EVM y su conexión con el ecosistema Polkadot.

* **Inmutabilidad:** Registro inmutable de hashes de validación y CIDs.


## 🔒 Almacenamiento & Privacidad

* **IPFS:** Datos sensibles encriptados y almacenados descentralizadamente.

* **Validación Off-Chain:** Mediante nodos propios (emulación TEE) con roadmap hacia integración futura de Phala Network.


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

[x] Diseño de Arquitectura EVM (Astar).

[x] Desarrollo de Web App (PWA) básica.

[ ] Implementación de Fuzzy Extractor en Cliente.

[ ] Integración con IPFS para evidencias encriptadas.

[ ] Despliegue de contratos en Shibuya Testnet.

[ ] Piloto con 5 ONGs en el Gran Chaco.


## 🤝 Contribuir

**¡Las contribuciones son bienvenidas!** Si eres desarrollador y te interesa el impacto social Web3:
Haz un Fork del proyecto.

Crea tu rama de funcionalidad (git checkout -b feature/AmazingFeature).
Haz Commit de tus cambios (git commit -m 'Add some AmazingFeature').
Haz Push a la rama (git push origin feature/AmazingFeature).
Abre un Pull Request.


## 📞 Contacto & Comunidad
¿Tienes dudas técnicas o quieres integrar tu ONG?

📧 Email Desarrolladores: developers@keyprotocol.ar

🐦 Twitter/X: @key_protocol

🌍 Website: keyprotocol.ar

<br />
<p align="center">
<sub>Desarrollado con ❤️ en el Gran Chaco Argentino by KEY protocol. Powered by Fundacion Gran Chaco, UTN, Latin Hack & NERDCONF.</sub>
</p>


