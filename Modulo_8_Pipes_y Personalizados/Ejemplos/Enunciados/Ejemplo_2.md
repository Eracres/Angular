# 🧪 Ejemplo 2: Uso del pipe `uppercase` en plantillas

## 🎯 Objetivo

Aplicar el pipe `uppercase` para transformar texto a mayúsculas directamente desde la plantilla HTML.

---

## 📁 Ruta: src/app/pipes/palabra.component.ts

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-palabra',
  templateUrl: './palabra.component.html'
})
export class PalabraComponent {
  mensaje: string = 'angular es genial';
}
```

---

## 📁 Ruta: src/app/pipes/palabra.component.html

```html
<p>{{ mensaje | uppercase }}</p>
```

---

## ✅ ¿Qué hace este componente?

Este ejemplo muestra cómo aplicar el pipe `uppercase` para **convertir una cadena de texto a mayúsculas** desde el HTML.  
El pipe se invoca con `|` seguido del nombre (`uppercase`) y puede encadenarse con otros pipes si es necesario.

---

## 🧠 Conceptos aplicados

- Uso de pipes incorporados en Angular
- Transformación visual de datos desde la plantilla
- Separación de presentación y lógica

---

## 💡 Variaciones sugeridas

### ✅ 1. Encadenar con `slice` para mostrar solo parte del texto en mayúsculas

```html
<p>{{ mensaje | uppercase | slice:0:7 }}</p>
```

📌 **¿Por qué?**: Esto permite aplicar varias transformaciones en cadena desde la plantilla.

---

### ✅ 2. Reemplazar por el pipe `titlecase`

```html
<p>{{ mensaje | titlecase }}</p>
```

📌 **¿Por qué?**: El pipe `titlecase` pone en mayúscula la primera letra de cada palabra (estilo título).

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Carga el componente en la vista principal (`<app-palabra>`).
2. Asegúrate de que el texto original está en minúsculas.
3. Comprueba en el navegador que se visualiza completamente en mayúsculas.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](./Ejemplo_3.md)  
### 🧪 - [Volver a Ejemplos](../README.md)  
### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)  
### 📘 - [Volver a Módulo 8](../../Modulo_8.md)  
### 🏠 - [Inicio](../../../README.md)

