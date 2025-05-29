# 🧪 Ejemplo 4: ngClass – Aplicar clases condicionales

## 🎯 Objetivo
Aplicar clases condicionales con `ngClass` según una variable booleana.


## `estilo.component.ts`
```ts
export class EstiloComponent {
  error: boolean = true;
}
```

## `estilo.component.html`
```html
<p [ngClass]="{ 'rojo': error, 'verde': !error }">Mensaje con estilo condicional</p>
```

## ✅ ¿Qué hace este componente?
Este componente aplica clases CSS dinámicamente según el valor de `error`, usando `ngClass`.

---

## ✅ ¿Cómo verificar que funciona correctamente?

Activa y desactiva la variable booleana desde el componente y verifica el cambio de estilo en pantalla.


## 🧠 Conceptos aplicados
- Uso de `ngClass` para estilos condicionales
- Binding de clases basado en lógica booleana
- Separación de lógica y estilos


---

## 💡 Variaciones sugeridas
```ts
Agregar más clases: `'subrayado': true`
```
```ts
Controlar con botón: `<button (click)=\"error = !error\">Toggle error</button>`
```


---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](./Ejemplo_5.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 3](../../Modulo_3.md)

### 🏠 - [Inicio](../../../README.md)


