# 🧪 Ejemplo 2: *ngFor – Listado de elementos

## 🎯 Objetivo
Utilizar la directiva `*ngFor` para iterar sobre una lista de elementos y renderizarlos dinámicamente en la plantilla.

## 📁 Ruta: src/app/lista/lista.component.ts
```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-lista',
  templateUrl: './lista.component.html'
})
export class ListaComponent {
  frutas = ['Manzana', 'Banana', 'Naranja'];
}
```

## 📁 Ruta: src/app/lista/lista.component.html
```html
<ul>
  <li *ngFor="let fruta of frutas">{{ fruta }}</li>
</ul>
```

---

## ✅ ¿Qué hace este componente?

Este ejemplo muestra cómo usar la directiva estructural `*ngFor` para generar una lista dinámica.  
Cada elemento del array `frutas` se imprime como un ítem (`<li>`) dentro del HTML.  
Esto es útil cuando se trabaja con datos dinámicos que necesitan ser renderizados en tiempo real, como resultados de una API.

---

## 🧠 Conceptos aplicados

- Directiva estructural `*ngFor`
- Iteración sobre arreglos en plantillas Angular
- Interpolación de valores dinámicos
- Separación de lógica (componente) y vista (plantilla)

---

## 💡 Variaciones sugeridas

### ✅ 1. Mostrar el índice junto a cada elemento

```html
<li *ngFor="let fruta of frutas; let i = index">{{ i + 1 }}. {{ fruta }}</li>
```

📌 **¿Por qué?**: Útil para numerar ítems o mantener referencia al índice actual.

---

### ✅ 2. Iterar sobre un array de objetos

```ts
frutas = [
  { nombre: 'Manzana', color: 'Rojo' },
  { nombre: 'Banana', color: 'Amarillo' },
  { nombre: 'Naranja', color: 'Naranja' }
];
```

```html
<li *ngFor="let fruta of frutas">
  {{ fruta.nombre }} - {{ fruta.color }}
</li>
```

📌 **¿Por qué?**: Muestra cómo manejar estructuras de datos más complejas.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Asegúrate de que el componente esté declarado en el módulo.
2. Visualiza el componente en la app usando su selector (`<app-lista>`).
3. Prueba agregar o quitar elementos del array y verifica que la lista se actualiza dinámicamente.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](./Ejemplo_3.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 3](../../Modulo_3.md)

### 🏠 - [Inicio](../../../README.md)

