# 🧪 Ejemplo 1: Configuración de un pipe personalizado

## 🎯 Objetivo

Crear un pipe personalizado en Angular que aplique un descuento porcentual a un precio numérico.

---

## 📁 Ruta: src/app/pipes/descuento.pipe.ts

```ts
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({ name: 'descuento' })
export class DescuentoPipe implements PipeTransform {
  transform(valor: number, porcentaje: number): number {
    return valor - (valor * porcentaje / 100);
  }
}
```

---

## 📁 Ruta: src/app/pipes/precio.component.ts

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-precio',
  templateUrl: './precio.component.html'
})
export class PrecioComponent {
  precioOriginal: number = 100;
}
```

---

## 📁 Ruta: src/app/pipes/precio.component.html

```html
<p>Precio con 20% de descuento: {{ precioOriginal | descuento:20 }}€</p>
```

---

## ✅ ¿Qué hace este componente?

Este ejemplo muestra cómo **crear y aplicar un pipe personalizado** llamado `descuento`.  
Este pipe toma un número (precio) y le aplica un porcentaje de descuento.  
El resultado es un valor numérico reducido, útil para mostrar precios finales directamente desde la plantilla.

---

## 🧠 Conceptos aplicados

- Decorador `@Pipe` para definir un pipe personalizado
- Implementación de `PipeTransform` con parámetros
- Uso de pipes personalizados en plantillas HTML

---

## 💡 Variaciones sugeridas

### ✅ 1. Aplicar descuento dinámico desde el componente

```ts
precioOriginal: number = 150;
porcentajeDescuento: number = 15;
```

```html
<p>{{ precioOriginal | descuento:porcentajeDescuento }}€</p>
```

📌 **¿Por qué?**: Permite mayor flexibilidad y reutilización al cambiar el descuento desde la lógica del componente.

---

### ✅ 2. Encadenar con `currency` para mostrarlo con formato de moneda

```html
<p>{{ precioOriginal | descuento:20 | currency }}</p>
```

📌 **¿Por qué?**: Mejora la presentación del resultado en la interfaz de usuario.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Declara `DescuentoPipe` en el módulo (`declarations`).
2. Utiliza `<app-precio>` en la vista principal.
3. Asegúrate de que el resultado del cálculo se actualiza correctamente según el porcentaje.

---

## 🔁 Navegación

### 🧪 - Ejemplo 2 [➡️](./Ejemplo_2.md)  
### 🧪 - [Volver a Ejemplos](../README.md)  
### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)  
### 📘 - [Volver a Módulo 8](../../Modulo_8.md)  
### 🏠 - [Inicio](../../../README.md)

