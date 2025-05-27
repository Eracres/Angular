# 🧪 Ejemplo 4: Ruta con parámetros dinámicos

## `producto.component.ts`
```ts
import { ActivatedRoute } from '@angular/router';
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-producto',
  templateUrl: './producto.component.html'
})
export class ProductoComponent implements OnInit {
  id: string | null = '';

  constructor(private route: ActivatedRoute) {}

  ngOnInit() {
    this.id = this.route.snapshot.paramMap.get('id');
  }
}
```

## `producto.component.html`
```html
<p>Mostrando detalles del producto con ID: {{ id }}</p>
```

## ✅ ¿Qué hace este componente?
Este componente captura el parámetro `id` de la ruta y lo muestra usando `ActivatedRoute`.

---

## 🧠 Conceptos aplicados
- Parámetros dinámicos en rutas
- Uso de `ActivatedRoute`
- Recuperar parámetros con `paramMap.get()`


---

## 💡 Variaciones sugeridas
```ts
Mostrar más propiedades (nombre, descripción) según el ID
```
```ts
Usar `paramMap.subscribe` para rutas dinámicas reactivas
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](./Ejemplo_5.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 4](../../Modulo_4.md)

### 🏠 - [Inicio](../../../README.md)
