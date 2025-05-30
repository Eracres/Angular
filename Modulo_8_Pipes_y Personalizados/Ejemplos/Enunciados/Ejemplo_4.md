# 🧪 Ejemplo 4: Pipe personalizado para aplicar IVA

## 🎯 Objetivo
Crear un pipe personalizado que aplique un porcentaje de IVA sobre un precio base.

## 📁 Ruta: src/app/pipes/iva.pipe.ts
```ts
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({ name: 'iva' })
export class IvaPipe implements PipeTransform {
  transform(valor: number, porcentaje: number = 21): number {
    return valor + (valor * porcentaje / 100);
  }
}
```

## 📁 Ruta: src/app/app.component.ts
```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html'
})
export class AppComponent {
  precioBase = 100;
}
```

## 📁 Ruta: src/app/app.component.html
```html
<p>Precio con IVA (21%): {{ precioBase | iva }}</p>
<p>Precio con IVA (10%): {{ precioBase | iva:10 }}</p>
```

---

## ✅ ¿Qué hace este componente?

Este ejemplo muestra cómo crear y utilizar un pipe personalizado para calcular el precio con IVA.  
El pipe `iva` recibe un número y le aplica un porcentaje adicional configurable.  
Por defecto se aplica el 21%, pero puede ajustarse en la plantilla.

---

## 🧠 Conceptos aplicados

- Creación de pipes personalizados con `@Pipe`
- Implementación de la interfaz `PipeTransform`
- Aplicación de lógica de transformación reutilizable
- Paso de argumentos a pipes

---

## 💡 Variaciones sugeridas

### ✅ 1. Mostrar precio sin decimales

```ts
return Math.round(valor + (valor * porcentaje / 100));
```

📌 ¿Por qué?: Mejora la presentación en interfaces sin requerir precisión decimal.

---

### ✅ 2. Aplicar descuento en lugar de IVA

```ts
return valor - (valor * porcentaje / 100);
```

📌 ¿Por qué?: Puedes invertir la lógica del pipe para reutilizarlo como "descuento".

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Declara el pipe en el módulo (`declarations`).
2. Usa el pipe en la plantilla con distintas tasas de IVA.
3. Comprueba que los valores se actualizan correctamente con los porcentajes proporcionados.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](./Ejemplo_5.md)
### 🧪 - [Volver a Ejemplos](../README.md)
### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)
### 📘 - [Volver a Módulo 8](../../Modulo_8.md)
### 🏠 - [Inicio](../../../README.md)

