# 🧪 Ejemplo 1: Interpolación básica

## `app.component.ts`
```ts
export class AppComponent {
  titulo = 'Angular Básico';
}
```

## `app.component.html`
```html
<h1>{{ titulo }}</h1>
```

## ✅ ¿Qué hace este componente?
Este componente muestra un título dinámico utilizando **interpolación**: el valor de `titulo` se inserta directamente en la vista.

---

## 🧠 Conceptos aplicados
- Interpolación con `{{ }}`
- Separación de lógica y vista
- Declaración de propiedades en la clase del componente


---

## 💡 Variaciones sugeridas
```ts
titulo = 'Hola Angular';
```
```ts
Concatenar texto: `{{ 'Bienvenido a ' + titulo }}`
```


---

## 🔁 Navegación

### 📘 [Volver a Módulo 2](../../Modulo_2.md)

### 📋 [Ir a Ejercicios](../../Ejercicios/Enunciados/README.md)

### 🏠 [Inicio](../README.md)
