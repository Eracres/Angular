# 🧪 Ejemplo 3: Event binding

## 🎯 Objetivo
Aprender a manejar eventos del usuario como clics usando la sintaxis `(evento)`.

## 📁 Ruta: src/app/app.component.ts
```ts
export class AppComponent {
  mostrarMensaje() {
    alert('¡Hola desde Angular!');
  }
}
```

## 📁 Ruta: src/app/app.component.html
```html
<button (click)="mostrarMensaje()">Haz clic aquí</button>
```

---

## ✅ ¿Qué hace este ejemplo?
Este ejemplo muestra cómo responder a un **evento DOM** como `click` ejecutando una función del componente.

---

## 🧠 Conceptos aplicados

- Event binding `(evento)`
- Vinculación de acciones del usuario a lógica del componente
- Manejo de funciones en Angular

---

## 💡 Variaciones sugeridas

### ✅ Mostrar datos en consola en lugar de alert
```ts
console.log('Botón clickeado');
```

📌 ¿Por qué?: Para pruebas sin mostrar ventanas emergentes.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Ejecuta la app.
2. Haz clic en el botón.
3. Debe aparecer un `alert` con el mensaje definido.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](./Ejemplo_4.md)
### 🧪 - [Volver a Ejemplos](../README.md)
### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)
### 📘 - [Volver a Módulo 2](../../Modulo_2.md)
### 🏠 - [Inicio](../../../README.md)

