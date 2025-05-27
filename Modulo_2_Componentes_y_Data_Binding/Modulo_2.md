# 📘 Módulo 2: Componentes y Data Binding en Angular

## 🧩 ¿Qué es el Data Binding?

El **Data Binding** en Angular permite enlazar datos entre el componente (TypeScript) y la vista (HTML). Angular ofrece 4 tipos principales de enlaces:

---

## 🔗 Tipos de Binding

### ✅ 1. Interpolación (`{{ variable }}`)

Permite mostrar valores de variables directamente en el HTML.
```html
<p>{{ mensaje }}</p>
```

### ✅ 2. Property Binding (`[propiedad]`)

Se usa para enlazar propiedades del DOM con datos del componente.
```html
<img [src]="imagenUrl">
```

### ✅ 3. Event Binding (`(evento)`)

Permite reaccionar a eventos del usuario.
```html
<button (click)="hacerAlgo()">Click</button>
```

### ✅ 4. Two-way Binding (`[(ngModel)]`)

Vincula el valor de una variable a un campo de formulario y viceversa.
```html
<input [(ngModel)]="usuario">
```

---

## 📦 Requisitos para usar `ngModel`

Para utilizar `[(ngModel)]` necesitas importar `FormsModule` en `app.module.ts`:

```ts
import { FormsModule } from '@angular/forms';

@NgModule({
  imports: [ FormsModule ],
})
export class AppModule { }
```

---

## 🧠 Ventajas del Data Binding

- Permite interfaces dinámicas y reactivas
- Facilita la separación entre lógica y vista
- Es declarativo y fácil de mantener

---

## 🧪 Ejemplo práctico

```ts
nombre = 'Laptop Gamer';
precio = 1500;
mostrarInfo() {
  alert(`Producto: ${this.nombre}`);
}
```

```html
<h3>{{ nombre }}</h3>
<p>{{ precio }}</p>
<button (click)="mostrarInfo()">Ver detalles</button>
```

---

## 🧪 Ejemplos de este módulo

* [🧪 Ejemplos del Módulo 2](./Ejemplos_Modulo_2.md)

---

## 📋 Ejercicios propuestos

* [📋 Ejercicios del Módulo 2](./Ejercicios_Modulo_2.md)

---

## 🔁 Navegación

⬅️ [Módulo 1](./Modulo_1.md) | ➡️ [Módulo 3](./Modulo_3.md)

🏠 [Volver al Inicio](../README.md)
