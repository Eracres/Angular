# 🧪 Ejemplo 2: Property binding

## 🎯 Objetivo
Entender cómo enlazar propiedades de elementos HTML con propiedades del componente usando `[property]`.

## 📁 Ruta: src/app/app.component.ts
```ts
export class AppComponent {
  imagenUrl: string = 'https://via.placeholder.com/150';
}
```

## 📁 Ruta: src/app/app.component.html
```html
<img [src]="imagenUrl" alt="Imagen dinámica">
```

---

## ✅ ¿Qué hace este ejemplo?
Este ejemplo demuestra cómo usar **property binding** para asignar dinámicamente valores a atributos HTML desde el componente.

---

## 🧠 Conceptos aplicados

- Property binding con `[atributo]`
- Comunicación del componente con la vista
- Renderizado dinámico de atributos

---

## 💡 Variaciones sugeridas

### ✅ Mostrar una segunda imagen si falla la primera
```html
<img [src]="imagenUrl || 'assets/imagen-default.jpg'">
```

📌 ¿Por qué?: Puedes manejar condiciones o valores alternativos desde la vista.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Asegúrate de que `imagenUrl` contiene una URL válida.
2. Si cambias su valor, la imagen debe actualizarse automáticamente en el navegador.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](./Ejemplo_3.md)
### 🧪 - [Volver a Ejemplos](../README.md)
### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)
### 📘 - [Volver a Módulo 2](../../Modulo_2.md)
### 🏠 - [Inicio](../../../README.md)
