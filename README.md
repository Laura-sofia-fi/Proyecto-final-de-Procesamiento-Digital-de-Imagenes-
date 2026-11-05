# Mejora de Imágenes con Baja Iluminación mediante Algoritmos Retinex en Java

Este repositorio contiene la implementación y comparación de algoritmos basados en la teoría centro-envolvente (*center/surround*) de **Retinex** desarrollados en **Java** para **ImageJ / Fiji**. El proyecto busca mejorar el contraste, corregir el balance de blancos y preservar la fidelidad del color en imágenes digitales capturadas en condiciones de baja iluminación[cite: 1].

## 📌 Descripción General
Basado en el principio de constancia del color de Land & McCann ($Imagen = Reflectancia \times Iluminación$), el proyecto realiza la estimación de iluminación en el dominio logarítmico para extraer la reflectancia de la escena[cite: 1]. Se implementan y analizan 4 variantes principales:

* **SSR** (*Single-Scale Retinex*): Evaluado en distintas escalas de desviación gaussiana ($\sigma \in \{15, 80, 250\}$)[cite: 1].
* **MSR** (*Multi-Scale Retinex*): Combinación ponderada de múltiples escalas para equilibrar detalles locales y contraste global[cite: 1].
* **MSRCR** (*Multi-Scale Retinex with Color Restoration*): Ajuste cromático para corregir la desaturación o aspecto grisáceo mediante funciones de cromaticidad y recorte de histograma (*simplest color balance*)[cite: 1].
* **MSRCP** (*Multi-Scale Retinex with Color Preservation*): Procesamiento enfocado en el canal de intensidad para mantener intactas las proporciones relativas de color[cite: 1].

## 🛠️ Tecnologías y Entorno
* **Lenguaje:** Java (JDK 8+)
* **Plataforma / Ecosistema:** ImageJ / Fiji (uso de `ij.ImagePlus`, `ij.process.ImageProcessor` y API de procesamiento digital de imágenes)[cite: 1].
* **Integración de IA (En desarrollo):** Modelos auxiliares para estimación adaptativa de iluminación[cite: 1].

## 🔬 Objetivos
1. Desplegar un plugin o script ejecutable en **ImageJ** para la evaluación cuantitativa y visual de los algoritmos Retinex[cite: 1].
2. Analizar el rendimiento computacional de la convolución gaussiana y operaciones de matriz de píxeles en Java[cite: 1].
3. Comparar el comportamiento de MSRCR y MSRCP en imágenes monocromáticas vs. escenas multicolor con baja iluminación[cite: 1].
