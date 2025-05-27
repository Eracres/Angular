# 🧪 Ejemplo 6: Checkbox con ngModel

## `app.component.ts`
```ts
export class AppComponent {
  suscrito = false;
}
```

## `app.component.html`
```html
<label>
  <input type="checkbox" [(ngModel)]="suscrito" />
  ¿Deseas suscribirte?
</label>
<p *ngIf="suscrito">¡Gracias por suscribirte!</p>
```

## ✅ ¿Qué hace este componente?
Este componente vincula un checkbox a una variable booleana con `[(ngModel)]` y muestra un mensaje condicional con `*ngIf`.

---

## 🧠 Conceptos aplicados
- Checkbox con binding bidireccional
- Uso de estructuras condicionales (`*ngIf`)
- Control de flujo visual en la vista

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_5.md) Ejemplo 5 - Modulo 3 [➡️](../../../Modulo_3_Directivas_Angular/Modulo_3.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 2](../../Modulo_2.md)

### 🏠 - [Inicio](../../../README.md)
