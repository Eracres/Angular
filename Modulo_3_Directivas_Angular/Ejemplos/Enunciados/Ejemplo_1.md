# 🧪 Ejemplo 1: *ngIf – Mostrar elemento condicionalmente

## 🎯 Objetivo
Aplicar una directiva estructural `*ngIf` para mostrar un mensaje condicionalmente.


## `condicional.component.ts`
```ts
export class CondicionalComponent {
  mostrar: boolean = true;
}
```

## `condicional.component.html`
```html
<p *ngIf="mostrar">Este mensaje solo se muestra si 'mostrar' es true</p>
```

## ✅ ¿Qué hace este componente?
Este componente utiliza `*ngIf` para mostrar un párrafo solo cuando la variable `mostrar` es verdadera.

---

## ✅ ¿Cómo verificar que funciona correctamente?

Cambia el valor de `mostrarMensaje` en el componente y observa si aparece o desaparece el contenido HTML.


## 🧠 Conceptos aplicados
- Uso de directiva estructural `*ngIf`
- Control de visibilidad basado en lógica
- Simplificación del DOM condicional


---

## 💡 Variaciones sugeridas
```ts
mostrar = false;
```
```ts
<button (click)="mostrar = !mostrar">Alternar visibilidad</button>
```


---

## 🔁 Navegación

### 🧪 - Ejemplo 2 [➡️](./Ejemplo_2.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 3](../../Modulo_3.md)

### 🏠 - [Inicio](../../../README.md)
