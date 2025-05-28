# 🧪 Ejemploc 4: Servicio con lógica para carrito

## `carrito.service.ts`
```ts
@Injectable({ providedIn: 'root' })
export class CarritoService {
  carrito: any[] = [];

  agregar(item: any) {
    this.carrito.push(item);
  }

  obtenerCarrito() {
    return this.carrito;
  }
}
```

## `carrito.component.ts`
```ts
@Component({...})
export class CarritoComponent {
  constructor(public carritoService: CarritoService) {}
}
```

## `carrito.component.html`
```html
<ul>
  <li *ngFor="let item of carritoService.carrito">
    {{ item.nombre }} - ${{ item.precio }}
  </li>
</ul>
```

## ✅ ¿Qué hace este componente?
Implementa una lógica de carrito accesible globalmente mediante un servicio.

---

## 🧠 Conceptos aplicados
- Gestión de estado simple
- Encapsulamiento de lógica en servicio
- Visualización con *ngFor

---

## 💡 Variaciones sugeridas
```ts
Método para eliminar producto del carrito
```

---
## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](./Ejemplo_5.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 5](../../Modulo_5.md)

### 🏠 - [Inicio](../../../README.md)

