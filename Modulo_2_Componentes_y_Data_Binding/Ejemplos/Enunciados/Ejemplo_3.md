# 🧪 Ejemplo 3: Event binding

## `app.component.ts`
```ts
export class AppComponent {
  mostrarMensaje() {
    alert('¡Has hecho clic!');
  }
}
```

## `app.component.html`
```html
<button (click)="mostrarMensaje()">Click aquí</button>
```

## ✅ ¿Qué hace este componente?
Este componente reacciona a eventos del usuario con **event binding**. Al hacer clic, se ejecuta una función del componente.

---

## 🧠 Conceptos aplicados
- Manejo de eventos DOM
- event binding con `(evento)`
- Ejecución de funciones del componente


---

## 💡 Variaciones sugeridas
```ts
console.log('Clic detectado');
```
```ts
Cambiar mensaje: alert('¡Gracias por hacer clic!');
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](./Ejemplo_4.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 2](../../Modulo_2.md)

### 🏠 - [Inicio](../../../README.md)
