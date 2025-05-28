# 🧪 Ejemplo 2: Inyección de servicio en componente

## `productos.component.ts`
```ts
import { Component, OnInit } from '@angular/core';
import { ProductoService } from '../servicios/producto.service';

@Component({
  selector: 'app-productos',
  templateUrl: './productos.component.html'
})
export class ProductosComponent implements OnInit {
  productos = [];

  constructor(private productoService: ProductoService) {}

  ngOnInit() {
    this.productos = this.productoService.obtenerProductos();
  }
}
```

## `productos.component.html`
```html
<ul>
  <li *ngFor="let prod of productos">{{ prod.nombre }} - ${{ prod.precio }}</li>
</ul>
```

## ✅ ¿Qué hace este componente?
Inyecta un servicio dentro del componente y accede a sus datos en el ciclo de vida `ngOnInit`.

---

## 🧠 Conceptos aplicados
- Inyección de dependencias
- Uso de servicios en componentes
- Ciclo de vida ngOnInit

---

## 💡 Variaciones sugeridas
```ts
// Agregar filtro para mostrar productos por precio
this.productos = this.productos.filter(p => p.precio > 30);
```

---
## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](./Ejemplo_3.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 5](../../Modulo_5.md)

### 🏠 - [Inicio](../../../README.md)

