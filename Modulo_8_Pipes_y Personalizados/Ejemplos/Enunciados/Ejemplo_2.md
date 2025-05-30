# 🧪 Ejemplo 2: Uso de servicio en componente

## 🎯 Objetivo
Inyectar un servicio en un componente para obtener datos centralizados.

## 📁 Ruta: src/app/producto.service.ts
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

## 📁 Ruta: src/app/listado/listado.component.ts
```ts
import { Component, OnInit } from '@angular/core';
import { ProductoService } from '../producto.service';

@Component({
  selector: 'app-listado',
  templateUrl: './listado.component.html'
})
export class ListadoComponent implements OnInit {
  productos: any[] = [];

  constructor(private productoService: ProductoService) {}

  ngOnInit() {
    this.productos = this.productoService.obtenerProductos();
  }
}
```

## 📁 Ruta: src/app/listado/listado.component.html
```html
<ul>
  <li *ngFor="let producto of productos">
    {{ producto.nombre }} - ${{ producto.precio }}
  </li>
</ul>
```

---

## ✅ ¿Qué hace este ejemplo?

Este componente muestra cómo inyectar un servicio (`ProductoService`) y consumir un método (`obtenerProductos()`) para cargar dinámicamente datos y mostrarlos en una lista HTML.

---

## 🧠 Conceptos aplicados

- Inyección de dependencias en el constructor
- Llamadas a métodos del servicio
- Binding e iteración con `*ngFor`

---

## 💡 Variaciones sugeridas

### ✅ 1. Usar `ngOnInit` para inicializar datos

```ts
ngOnInit() {
  this.productos = this.productoService.obtenerProductos();
}
```
📌 **¿Por qué?**: Es el ciclo de vida recomendado para inicializar datos.

---

### ✅ 2. Agregar un botón para actualizar productos

```html
<button (click)="cargarProductos()">Recargar</button>
```

```ts
cargarProductos() {
  this.productos = this.productoService.obtenerProductos();
}
```
📌 **¿Por qué?**: Permite recargar los datos bajo demanda.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Verifica que el servicio `ProductoService` esté bien importado.
2. Comprueba que el array `productos` se carga en el `ngOnInit`.
3. Asegúrate de que los datos se renderizan correctamente con `*ngFor`.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](./Ejemplo_3.md)
### 🧪 - [Volver a Ejemplos](../README.md)
### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)
### 📘 - [Volver a Módulo 5](../../Modulo_5.md)
### 🏠 - [Inicio](../../../README.md)

