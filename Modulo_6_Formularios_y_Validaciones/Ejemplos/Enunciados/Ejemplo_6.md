# 🧪 Ejemplo 6: Formulario completo de contacto

## `formulario.component.ts`
```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-formulario',
  templateUrl: './formulario.component.html',
})
export class FormularioComponent {
  nombre: string = '';
  email: string = '';
  mensaje: string = '';

  enviar() {
    alert(`Mensaje enviado por ${this.nombre}`);
  }
}
```

## `formulario.component.html`
```html
<form (ngSubmit)="enviar()">
  <label>Nombre:</label>
  <input [(ngModel)]="nombre" name="nombre" required><br>

  <label>Email:</label>
  <input type="email" [(ngModel)]="email" name="email" required><br>

  <label>Mensaje:</label>
  <textarea [(ngModel)]="mensaje" name="mensaje" required></textarea><br>

  <button type="submit">Enviar</button>
</form>
```

## ✅ ¿Qué hace este componente?
Este componente implementa un formulario completo de contacto con campos validados y envío por botón.

---

## 🧠 Conceptos aplicados
- Template-driven forms
- Validaciones básicas con `required`
- Evento `ngSubmit`
- Uso de `textarea`, inputs y `button`

---

## 💡 Variaciones sugeridas

```html
<!-- Mostrar resumen del mensaje al enviar -->
<div *ngIf="mensajeEnviado">
  Gracias por tu mensaje, {{ nombre }}.
</div>
```

```ts
// Agregar validación más avanzada por método
validarFormulario() {
  // Lógica personalizada
}
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_5.md) Ejemplo 5 - Módulo 7 [➡️](../../../Modulo_7_Consumo_de_APIs_con_HttpClient/Modulo_7.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 6](../../Modulo_6.md)

### 🏠 - [Inicio](../../../README.md)

