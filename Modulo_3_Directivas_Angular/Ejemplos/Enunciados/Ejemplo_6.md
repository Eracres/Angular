# 🧪 Ejemplo 6: Combinando directivas

## `combinado.component.ts`
```ts
export class CombinadoComponent {
  elementos = ['HTML', 'CSS', 'Angular'];
  mostrar: boolean = true;
}
```

## `combinado.component.html`
```html
<ul *ngIf="mostrar">
  <li *ngFor="let e of elementos">{{ e }}</li>
</ul>
```

## ✅ ¿Qué hace este componente?
Este componente combina `*ngIf` y `*ngFor` para mostrar una lista solo cuando `mostrar` es verdadero.

---

## 🧠 Conceptos aplicados
- Combinación de `*ngIf` y `*ngFor`
- Renderizado condicional y dinámico
- Buenas prácticas de estructuración


---

## 💡 Variaciones sugeridas
```ts
Cambiar la condición: `mostrar = false;`
```
```ts
Alternar visibilidad con botón
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_5.md) Ejemplo 5 - Modulo 4 [➡️](../../../Modulo_4_/Modulo_4.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 3](../../Modulo_3.md)

### 🏠 - [Inicio](../../../README.md)
