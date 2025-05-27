# 🧪 Ejemplo 1: Componente básico con interpolación

## `saludo.component.ts`
```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-saludo',
  templateUrl: './saludo.component.html',
  styleUrls: ['./saludo.component.css']
})
export class SaludoComponent {
  nombre: string = 'Estudiante';
}
```

## `saludo.component.html`
```html
<h2>Hola, {{ nombre }} 👋</h2>
```

## ✅ ¿Qué hace este componente?
Este componente muestra un mensaje dinámico utilizando **interpolación**: el valor de la variable `nombre` se inserta directamente en el HTML.

---

## 🧠 Conceptos aplicados
- Creación de componentes con Angular CLI
- Enlace unidireccional de datos (One-way data binding)
- Separación de lógica y presentación

---

## 💡 Variaciones sugeridas

```ts
// Cambia el valor
nombre: string = 'Lucía';
```

```ts
// Hazlo dinámico desde el componente padre
@Input() nombre: string = '';
```

```html
<app-saludo [nombre]="'Carlos'"></app-saludo>
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_0.md) Ejemplo 0

### 🧪 - [Volver a Ejemplos](../README.md) 

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 1](../../Modulo_1.md)

### 🏠 - [Inicio](../../../README.md)
