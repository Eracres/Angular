# 🧪 Ejemplo 5: Binding combinado

## 🎯 Objetivo
Practicar la combinación de interpolación y event binding para mostrar y manipular datos desde la plantilla HTML.

## 📁 Ruta: src/app/app.component.ts

```ts
export class AppComponent {
  producto = 'Laptop Gamer';
  precio = 1500;
}
```

## 📁 Ruta: src/app/app.component.html

```html
<h2>{{ producto }}</h2>
<p>Precio: ${{ precio }}</p>
<button (click)="alert('Producto: ' + producto)">Ver</button>
```

---

## ✅ ¿Qué hace este componente?

Este componente combina dos técnicas fundamentales de Angular:  
- **Interpolación** para mostrar datos dinámicos como el nombre del producto y su precio.  
- **Event binding** para responder a eventos del usuario, como el clic en un botón.

---

## 🧠 Conceptos aplicados

- Interpolación con `{{ }}`
- Enlace de eventos con `(click)`
- Manipulación de eventos desde la vista

---

## 💡 Variaciones sugeridas

### ✅ 1. Agregar más propiedades

```ts
stock = 10;
marca = 'Asus';
```
📌 **¿Por qué?**: Para representar más detalles del producto.

---

### ✅ 2. Cambiar el mensaje del botón

```html
<button (click)="alert('Has elegido: ' + producto)">Seleccionar</button>
```
📌 **¿Por qué?**: Para personalizar la interacción con el usuario.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](./Ejemplo_6.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 2](../../Modulo_2.md)

### 🏠 - [Inicio](../../../README.md)
