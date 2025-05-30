# 🧪 Ejemplo 6: Uso combinado de múltiples pipes personalizados

## 🎯 Objetivo
Aplicar múltiples pipes personalizados encadenados en una expresión para transformar datos complejos.

## 📁 Ruta: src/app/pipes/nombre-completo.pipe.ts
```ts
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({ name: 'nombreCompleto' })
export class NombreCompletoPipe implements PipeTransform {
  transform(nombre: string, apellido: string): string {
    return `${nombre} ${apellido}`;
  }
}
```

## 📁 Ruta: src/app/pipes/mayusculas.pipe.ts
```ts
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({ name: 'mayusculas' })
export class MayusculasPipe implements PipeTransform {
  transform(valor: string): string {
    return valor.toUpperCase();
  }
}
```

## 📁 Ruta: src/app/app.component.ts
```ts
export class AppComponent {
  nombre = 'ana';
  apellido = 'pérez';
}
```

## 📁 Ruta: src/app/app.component.html
```html
<p>{{ nombre | nombreCompleto:apellido | mayusculas }}</p>
```

---

## ✅ ¿Qué hace este componente?

Este ejemplo muestra cómo encadenar múltiples **pipes personalizados**.  
Primero se utiliza `nombreCompleto` para unir nombre y apellido, y luego se aplica el pipe `mayusculas` para convertir el resultado a mayúsculas.

Esto permite realizar transformaciones complejas en el HTML de forma declarativa y reutilizable.

---

## 🧠 Conceptos aplicados

- Pipes personalizados encadenados
- Reutilización de lógica de transformación
- Lectura y composición declarativa en plantillas

---

## 💡 Variaciones sugeridas

### ✅ 1. Encadenar pipes con valores distintos

```html
<p>{{ 'juan' | nombreCompleto:'gómez' | mayusculas }}</p>
```

📌 **¿Por qué?**: Puedes aplicar pipes directamente a valores literales si no dependes de variables del componente.

---

### ✅ 2. Combinar con pipes nativos

```html
<p>{{ 'ana' | nombreCompleto:'pérez' | uppercase }}</p>
```

📌 **¿Por qué?**: También puedes usar pipes de Angular nativos en la cadena para una mayor flexibilidad.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Declara ambos pipes personalizados en `app.module.ts`.
2. Visualiza el resultado en el navegador.
3. Asegúrate de que el texto aparezca correctamente transformado.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_5.md) Ejemplo 5 - Ejemplo 6

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 8](../../Modulo_8.md)

### 🏠 - [Inicio](../../../README.md)

