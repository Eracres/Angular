# 🧪 Ejemplo 2: Uso de router-outlet

## `app.component.ts`
```ts
export class AppComponent {
  title = 'Mi App Angular';
}
```

## `app.component.html`
```html
<h1>{{ title }}</h1>
<router-outlet></router-outlet>
```

## ✅ ¿Qué hace este componente?
`<router-outlet>` actúa como un contenedor dinámico que muestra el componente activo según la ruta actual.

---

## 🧠 Conceptos aplicados
- Uso de `<router-outlet>` para el contenido enrutado
- Componentes cargados dinámicamente por ruta


---

## 💡 Variaciones sugeridas
```ts
Agregar `<nav>` con enlaces de navegación
```
```ts
Colocar `<router-outlet>` dentro de un layout principal
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](./Ejemplo_3.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 4](../../Modulo_4.md)

### 🏠 - [Inicio](../../../README.md)
