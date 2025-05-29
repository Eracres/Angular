# 🧪 Ejemplo 4: Two-way binding con ngModel

## 🎯 Objetivo
Aprender a sincronizar una variable del componente con un campo de entrada del usuario en tiempo real utilizando `[(ngModel)]`.

## 📁 Ruta: src/app/app.component.ts

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
})
export class AppComponent {
  nombre: string = '';
}
```

## 📁 Ruta: src/app/app.component.html

```html
<label>Nombre:
  <input [(ngModel)]="nombre" placeholder="Escribe tu nombre">
</label>
<p>Hola, {{ nombre }}</p>
```

---

## ✅ ¿Qué hace este componente?

Este ejemplo permite al usuario escribir su nombre en un campo de texto y ver el resultado en tiempo real en la interfaz gracias a la **vinculación bidireccional (two-way binding)** que ofrece Angular mediante `[(ngModel)]`.

---

## 🧠 Conceptos aplicados

- Uso de `FormsModule` para trabajar con formularios template-driven
- Two-way data binding con `[(ngModel)]`
- Interpolación de valores

---

## 💡 Variaciones sugeridas

### ✅ 1. Mostrar longitud del texto

```html
<p>Tu nombre tiene {{ nombre.length }} caracteres.</p>
```
📌 **¿Por qué?**: Para enseñar cómo acceder a propiedades de la variable vinculada.

---

### ✅ 2. Usar ngModel en una etiqueta `textarea`

```html
<textarea [(ngModel)]="mensaje" placeholder="Escribe tu mensaje"></textarea>
<p>Mensaje: {{ mensaje }}</p>
```
📌 **¿Por qué?**: Para demostrar que `[(ngModel)]` se puede usar con distintos elementos del formulario.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](./Ejemplo_5.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 2](../../Modulo_2.md)

### 🏠 - [Inicio](../../../README.md)
