# 🧪 Ejemplo 5: Mostrar errores condicionales

## `formulario.component.ts`
```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-formulario',
  templateUrl: './formulario.component.html',
})
export class FormularioComponent {
  email: string = '';
}
```

## `formulario.component.html`
```html
<form>
  <label>Email:</label>
  <input type="email" [(ngModel)]="email" name="email" required #emailInput="ngModel">
  <div *ngIf="emailInput.invalid && emailInput.touched">
    <small *ngIf="emailInput.errors?.['required']">El email es obligatorio.</small>
    <small *ngIf="emailInput.errors?.['email']">Formato inválido.</small>
  </div>
</form>
```

## ✅ ¿Qué hace este componente?
Este formulario muestra mensajes de error condicionales cuando el campo de email está vacío o mal escrito y ha sido tocado.

---

## 🧠 Conceptos aplicados
- `[(ngModel)]` y `name`
- Validación con `required` y `email`
- Directivas estructurales `*ngIf`
- Template reference variables (`#var`)

---

## 💡 Variaciones sugeridas

```html
<!-- Añadir validación personalizada -->
<input pattern="[a-z]+@[a-z]+\.[a-z]{2,3}" />
```

```html
<!-- Estilos de error con clases CSS -->
<div [class.error]="emailInput.invalid">...</div>
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](./Ejemplo_6.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 6](../../Modulo_6.md)

### 🏠 - [Inicio](../../../README.md)
