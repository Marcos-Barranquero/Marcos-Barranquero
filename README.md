# 👋 Hi, I'm Dr. Marcos Barranquero

**Senior Fullstack Engineer | Cloud Architect | PhD in Computer Science**

Welcome to my GitHub! I'm a software engineer passionate about building scalable, high-performance applications and solving complex architectural challenges. By combining my academic research background with hands-on experience managing critical enterprise infrastructure, I focus on delivering product-driven, clean, and efficient solutions.

### 🚀 About Me
- 🏛️ **Background:** PhD in Computer Engineering (*Cum Laude*). Thesis: *"Development of a Web Tool for Radio Coverage Calculation and Mobile Network Optimization"* — focused on high-performance 3D visualization, accelerated ray-tracing algorithms, and AI-driven urban reconstruction (LiDAR/CNNs).
- 💼 **Experience:** Currently designing and scaling critical backend microservices in the banking sector (handling 5,000+ requests/minute with high availability). 
- 🧠 **Mindset:** I thrive in product-oriented environments. I advocate for Clean Architecture, Developer Experience (DX).
- 🌱 **Currently exploring:** Advanced AI/LLM integrations (Ollama, Groq), the **T3 Stack** (Next.js, tRPC, Tailwind), and Agentic Coding.

### 💻 Tech Stack & Tools
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

### 📫 Let's Connect
- ✉️ **Email:** marcosbarranquero@outlook.es


Para crear una organización consumidora en un catálogo utilizando la CLI (apic-slim.exe), debes usar el comando consumer-orgs:create y proporcionarle un archivo de definición (o pasarle la entrada directamente a través de la línea de comandos) que contenga los detalles de la nueva organización.
Aquí tienes los pasos exactos para hacerlo:
1. Obtener la URL del propietario (owner_url)
Toda organización consumidora necesita un usuario propietario. Para el archivo de creación, necesitarás la URL exacta de ese usuario en el sistema. Puedes obtenerla ejecutando el siguiente comando:

./apic-slim.exe users:get <nombre_de_usuario> --user-registry <nombre_del_registro_de_usuarios> --server <servidor_gestion> --org <tu_organizacion_proveedora> --fields url --output -

Este comando te devolverá algo parecido a esto: https://<servidor>/api/user-registries/.../users/....
2. Ejecutar el comando de creación
Puedes crear la organización de dos formas: usando un archivo o insertando los datos directamente en la terminal.
Opción A: Pasando los datos directamente (stdin) Utiliza un guion (-) al final del comando para indicarle a la CLI que leerá la entrada desde la consola:

./apic-slim.exe consumer-orgs:create --server <servidor_gestion> --catalog <nombre_catalogo> --org <tu_organizacion_proveedora> -

Al presionar Enter, la consola esperará que introduzcas el contenido. Pega lo siguiente (sustituyendo los valores) y presiona CTRL+D para terminar la entrada:

name: mi-org-consumidora
title: Mi Organización Consumidora
owner_url: https://<servidor_gestion>/api/user-registries/.../users/fddd5df5-c178-4a34-ab92-0a48344d5c9b

Nota: name debe contener solo caracteres alfanuméricos, guiones y guiones bajos. title es el nombre legible para los usuarios.
Opción B: Usando un archivo de definición Si prefieres automatizarlo, guarda el bloque YAML (o su equivalente en JSON) del paso anterior en un archivo llamado, por ejemplo, consumer_org.yaml. Luego ejecuta:

./apic-slim.exe consumer-orgs:create --server <servidor_gestion> --catalog <nombre_catalogo> --org <tu_organizacion_proveedora> consumer_org.yaml

De esta forma, la organización consumidora quedará registrada bajo el catálogo especificado.
¿Cómo se configura un Test-ID en el YAML de Automated API behavior testing?
¿Qué categorías semánticas existen para las propiedades de una API Extension?
¿Cómo puedo usar JUnitFormat para integrar los tests en Jenkins?
