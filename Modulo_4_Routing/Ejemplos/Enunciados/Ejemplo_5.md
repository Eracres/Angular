# 🧪 Ejemplo 5: Página 404 personalizada

## `not-found.component.ts`
```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-not-found',
  templateUrl: './not-found.component.html'
})
export class NotFoundComponent {}
```

## `not-found.component.html`
```html
<h2>Página no encontrada 😢</h2>
<a routerLink="/">Volver al inicio</a>
```

## ✅ ¿Qué hace este componente?
Este componente se usa para manejar rutas no definidas, usando `path: '**'` en el router.

---

## 🧠 Conceptos aplicados
- Ruta comodín `**`
- Página de error personalizada
- Navegación de retorno


---

## 💡 Variaciones sugeridas
```ts
Agregar un botón con `routerLink`
```
```ts
Mostrar un diseño más llamativo con íconos o animaciones
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](./Ejemplo_6.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 4](../../Modulo_4.md)

### 🏠 - [Inicio](../../../README.md)

