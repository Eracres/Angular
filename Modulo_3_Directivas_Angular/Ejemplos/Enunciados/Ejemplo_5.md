# 🧪 Ejemplo 5: ngStyle – Estilos dinámicos

## `color.component.ts`
```ts
export class ColorComponent {
  colorTexto: string = 'blue';
}
```

## `color.component.html`
```html
<p [ngStyle]="{ 'color': colorTexto }">Este texto cambia de color</p>
```

## ✅ ¿Qué hace este componente?
Este componente utiliza `ngStyle` para modificar el estilo del texto dinámicamente desde el componente.

---

## 🧠 Conceptos aplicados
- Uso de `ngStyle` para estilo en línea
- Estilo reactivo controlado por variables
- Separación de lógica y vista


---

## 💡 Variaciones sugeridas
```ts
colorTexto = 'red';
```
```ts
Agregar más propiedades: `{ 'fontWeight': 'bold' }`
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](./Ejemplo_6.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 3](../../Modulo_3.md)

