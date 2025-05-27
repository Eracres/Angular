# 🧪 Ejemplo 2: Property binding

## `app.component.ts`
```ts
export class AppComponent {
  imagenUrl = 'https://via.placeholder.com/150';
}
```

## `app.component.html`
```html
<img [src]="imagenUrl" alt="Imagen dinámica" />
```

## ✅ ¿Qué hace este componente?
Este componente usa **property binding** para asignar dinámicamente una URL al atributo `src` de la imagen.

---

## 🧠 Conceptos aplicados
- Binding de atributos con `[]`
- Enlace unidireccional desde componente a vista

---

## 💡 Variaciones sugeridas
```ts
imagenUrl = 'https://picsum.photos/200';
```
```ts
<img [alt]="'Imagen de ' + imagenUrl" />
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](./Ejemplo_3.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/Enunciados/README.md)

### 📘 - [Volver a Módulo 2](../../Modulo_2.md)

### 🏠 - [Inicio](../../../README.md)
