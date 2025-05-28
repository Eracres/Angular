# 🧪 Ejemplo 1: Crear un servicio básico

## `producto.service.ts`
```ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class ProductoService {
  productos = [
    { id: 1, nombre: 'Teclado', precio: 50 },
    { id: 2, nombre: 'Mouse', precio: 25 }
  ];

  obtenerProductos() {
    return this.productos;
  }
}
```

## ✅ ¿Qué hace este componente?
Este servicio contiene un arreglo de productos y una función para devolverlos. Angular lo provee automáticamente a toda la app gracias a `providedIn: 'root'`.

---

## 🧠 Conceptos aplicados
- Creación de servicios con Angular CLI
- Uso de `@Injectable`
- Patrón de encapsulación de lógica

---

## 💡 Variaciones sugeridas
```ts
// Devolver productos como Observable
import { of } from 'rxjs';
obtenerProductos() {
  return of(this.productos);
}
```

```ts
// Incluir más propiedades en cada producto
{ id: 3, nombre: 'Monitor', precio: 200, stock: 10 }
```

---

## 🔁 Navegación

### 🧪 - Ejemplo 2 [➡️](./Ejemplo_2.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 5](../../Modulo_5.md)

### 🏠 - [Inicio](../../../README.md)
