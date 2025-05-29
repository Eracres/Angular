# 🧪 Ejemplo 3: *ngSwitch – Condición múltiple

## 🎯 Objetivo
Implementar `ngSwitch` para mostrar contenido diferente en función de un valor de control.


## `switch.component.ts`
```ts
export class SwitchComponent {
  nivel = 2;
}
```

## `switch.component.html`
```html
<div [ngSwitch]="nivel">
  <p *ngSwitchCase="1">Nivel uno</p>
  <p *ngSwitchCase="2">Nivel dos</p>
  <p *ngSwitchDefault>Desconocido</p>
</div>
```

## ✅ ¿Qué hace este componente?
Este componente utiliza `ngSwitch` para mostrar un contenido diferente según el valor de `nivel`.

---

## ✅ ¿Cómo verificar que funciona correctamente?

Cambia el valor de `opcionSeleccionada` y comprueba que se muestra la sección correspondiente.


## 🧠 Conceptos aplicados
- Uso de `ngSwitch`, `*ngSwitchCase` y `*ngSwitchDefault`
- Evaluación de múltiples condiciones
- Renderizado selectivo según valor


---

## 💡 Variaciones sugeridas
```ts
nivel = 1;
```
```ts
nivel = 3;
```


---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](./Ejemplo_4.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 3](../../Modulo_3.md)

### 🏠 - [Inicio](../../../README.md)

