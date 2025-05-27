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

### 🧪 - [⬅️](./Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](./Ejemplo_4.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 2](../../Modulo_2.md)

### 🏠 - [Inicio](../../../README.md)

