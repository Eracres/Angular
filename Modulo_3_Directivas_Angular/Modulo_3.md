
# 📘 Módulo 3: Directivas estructurales y de atributo

## ❓ ¿Qué son las directivas en Angular?

Las directivas son instrucciones que puedes aplicar sobre elementos del DOM para **alterar su comportamiento o apariencia**. En Angular, existen tres tipos:

### 1. **Directivas de componente**
- Son las más comunes. Todo componente es una directiva con plantilla.

### 2. **Directivas estructurales**
- Modifican la estructura del DOM. Se reconocen por el prefijo `*`.
- Ejemplos: `*ngIf`, `*ngFor`, `*ngSwitch`

### 3. **Directivas de atributo**
- Cambian el aspecto o comportamiento de un elemento sin modificar la estructura.
- Ejemplos: `ngClass`, `ngStyle`

---

## 📐 Directivas estructurales comunes

### ✅ `*ngIf`
Muestra u oculta un elemento en función de una condición booleana.
```html
<p *ngIf="activo">Usuario activo</p>
```

### ✅ `*ngFor`
Itera sobre una colección y genera un elemento por cada ítem.
```html
<li *ngFor="let item of items">{{ item }}</li>
```

### ✅ `*ngSwitch`
Evalúa múltiples condiciones.
```html
<div [ngSwitch]="valor">
  <p *ngSwitchCase="1">Uno</p>
  <p *ngSwitchCase="2">Dos</p>
  <p *ngSwitchDefault>No coincide</p>
</div>
```

---

## 🎨 Directivas de atributo comunes

### ✅ `ngClass`
Aplica clases CSS condicionalmente.
```html
<p [ngClass]="{ 'rojo': esError }">Texto</p>
```

### ✅ `ngStyle`
Aplica estilos CSS directamente desde el componente.
```html
<p [ngStyle]="{ 'color': colorTexto }">Texto</p>
```

---

## 🧠 ¿Qué ventajas tienen?

- Reutilización de lógica visual
- Código más limpio y mantenible
- Separación entre lógica y vista
- Mejora la legibilidad

---

## 🧪 Ejemplos de este módulo

#### [🔗 Listado de Ejemplos](./Ejemplos/README.md)

---

## 📋 Ejercicios propuestos

#### [🔗 Listado de Ejercicios](./Ejercicios/README.md)

---

## 🔁 Navegación

### 📘 - [⬅️](../Modulo_2_Componentes_y_Data_Binding/Modulo_2.md) Módulo 2 - Módulo 4 [➡️](../Modulo_4_Routing/Modulo_4.md)

### 🏠 [Inicio](../README.md)
