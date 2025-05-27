# 🧪 Ejemplo 3: Navegación con routerLink

## `app.component.ts`
```ts
export class AppComponent {}
```

## `app.component.html`
```html
<nav>
  <a routerLink="/">Inicio</a>
  <a routerLink="/acerca">Acerca</a>
</nav>
<router-outlet></router-outlet>
```

## ✅ ¿Qué hace este componente?
El atributo `routerLink` permite cambiar de ruta sin recargar la página, manteniendo la experiencia SPA.

---

## 🧠 Conceptos aplicados
- Enlace declarativo con `routerLink`
- Estilo de navegación SPA
- Separación de menú y contenido


---

## 💡 Variaciones sugeridas
```ts
Agregar clase activa con `routerLinkActive`
```
```ts
Agregar más enlaces como `/contacto`, `/servicios`
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](./Ejemplo_4.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 4](../../Modulo_4.md)

### 🏠 - [Inicio](../../../README.md)

