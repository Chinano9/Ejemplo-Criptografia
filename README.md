# Laboratorio de Cifrado Híbrido (AES + RSA)

Este repositorio contiene un prototipo interactivo y educativo que demuestra el funcionamiento del cifrado híbrido utilizando criptografía simétrica (AES) y asimétrica (RSA) directamente en el navegador.
## Objetivo

El objetivo de esta herramienta es visualizar el flujo completo de una comunicación segura sobre un canal inseguro. En lugar de ser un simple script, la aplicación simula a los tres actores clásicos de la criptografía:

* Alice (Emisor): Cifra el mensaje usando una llave de sesión rápida (AES) y protege esa llave temporal con la llave pública de Bob.

* El Canal Inseguro (Eve / Atacante): Muestra cómo los datos viajan por la red. Permite simular ataques de corrupción de datos y pérdida de sincronización.
* Bob (Receptor): Ejecuta el protocolo de Handshake para compartir su llave pública y utiliza su llave privada para descifrar el paquete de Alice.

## Características

* Handshake Visual: Generación de llaves RSA (1024 bits) en tiempo real.

* Cifrado Híbrido: Combinación de la velocidad de AES-128 para los datos y la robustez matemática de RSA para proteger la llave de sesión.

* Simulación de Ataques:
  * Pérdida de Integridad: Modifica un solo bit en tránsito para demostrar el "efecto avalancha" al romper el bloque AES.
  * Desincronización: Fuerza la regeneración de llaves asimétricas a mitad de camino para demostrar la falla matemática del sistema RSA.
  * Consola de Operaciones: Un log tipo terminal que explica paso a paso lo que sucede bajo el capó a nivel criptográfico.

## Stack Tecnológico

Siguiendo una filosofía de herramientas simples y funcionales, el prototipo está construido en un solo archivo .html (Cero dependencias de servidor):
* Criptografía: node-forge (Implementación robusta en JavaScript puro).
* UI/Diseño: Tailwind CSS (vía CDN) y FontAwesome para la iconografía.

## Cómo usarlo

Basta con clonar el repositorio y abrir index.html en cualquier navegador web moderno, o visitar la versión desplegada en vivo (a través de GitHub Pages).
