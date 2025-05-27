
# 📘 Módulo 1: Introducción a Angular

## ❓ ¿Qué es Angular?

Angular es un **framework frontend** desarrollado por Google para crear **Single Page Applications (SPA)**. Está construido en **TypeScript** y ofrece una arquitectura robusta basada en componentes, inyección de dependencias, y herramientas integradas para desarrollo profesional.

### ✅ ¿Qué ofrece Angular?
- Componentes reutilizables
- Módulos organizados
- Servicios e inyección de dependencias
- Routing para navegar sin recargar la página
- Soporte completo para formularios
- Interfaz reactiva con RxJS
- Herramientas para pruebas y rendimiento
- Ecosistema sólido y escalable

---

## 🔧 Instalación del entorno

### 1. Instalar Node.js
Descárgalo desde: [https://nodejs.org](https://nodejs.org)

### 2. Instalar Angular CLI (herramienta de línea de comandos)
```bash
npm install -g @angular/cli
```

### 3. Crear un nuevo proyecto Angular
```bash
ng new hola-angular
cd hola-angular
ng serve
```
Abre `http://localhost:4200` en tu navegador.

---

## 🗂️ Estructura del proyecto

| Archivo / Carpeta         | Función principal                                  |
|---------------------------|----------------------------------------------------|
| `src/`                    | Código fuente de la app                            |
| `src/app/`                | Módulo y componentes de la aplicación              |
| `app.module.ts`           | Módulo principal de la app                         |
| `app.component.ts/html`   | Componente raíz (vista inicial)                   |
| `main.ts`                 | Punto de entrada de la app                         |

---

## 🧩 Crear un componente

```bash
ng generate component saludo
```

Esto crea los archivos:
- `saludo.component.ts`: lógica del componente
- `saludo.component.html`: vista asociada
- `saludo.component.css`: estilos
- `saludo.component.spec.ts`: pruebas

---

## 🧪 Ejemplos de este módulo

* [🧪 Ejemplo 1: Componente básico con interpolación](./Ejemplos/README.md)

---

## 📋 Ejercicios propuestos

* [📋 Ejercicio 1: Bienvenida con interpolación](./Ejercicios/README.md)

---

## 🔁 Navegación

### Módulo 2 [➡️](../Modulo_2_Componentes_y_Data_Binding/Modulo_2.md)

### 🏠 [Volver al Inicio](../README.md)
