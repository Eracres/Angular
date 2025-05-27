# 🧪 Ejemplo 4: Two-way binding con ngModel

## `app.component.ts`
```ts
export class AppComponent {
  nombre: string = '';
}
```

## `app.component.html`
```html
<input [(ngModel)]="nombre" placeholder="Tu nombre">
<p>Hola, {{ nombre }}</p>
```

## ✅ ¿Qué hace este componente?
Este componente permite al usuario escribir su nombre en un input y lo muestra en tiempo real gracias a `[(ngModel)]`.

---

## 🧠 Conceptos aplicados
- Two-way binding con `[(ngModel)]`
- Actualización reactiva de datos
- Uso de formularios simples en Angular

---

## 💡 Variaciones sugeridas
```ts
placeholder = 'Escribe tu nombre';
```
```ts
Mostrar longitud del nombre: `{{ nombre.length }}`
```


---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](./Ejemplo_5.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 2](../../Modulo_2.md)

### 🏠 - [Inicio](../../../README.md)

