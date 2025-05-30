# 🧪 Ejemplo 3: Pipe personalizado para edad

## 🎯 Objetivo
Crear un pipe personalizado llamado `edad` que calcule la edad a partir de una fecha de nacimiento.

---

## 📁 Ruta: src/app/pipes/edad.pipe.ts
```ts
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({ name: 'edad' })
export class EdadPipe implements PipeTransform {
  transform(fechaNacimiento: string | Date): number {
    const hoy = new Date();
    const nacimiento = new Date(fechaNacimiento);
    let edad = hoy.getFullYear() - nacimiento.getFullYear();
    const m = hoy.getMonth() - nacimiento.getMonth();
    if (m < 0 || (m === 0 && hoy.getDate() < nacimiento.getDate())) {
      edad--;
    }
    return edad;
  }
}
```

---

## 📁 Ruta: src/app/app.component.html
```html
<p>Edad: {{ '1990-06-15' | edad }} años</p>
```

---

## ✅ ¿Qué hace este ejemplo?

Este pipe personalizado toma una fecha de nacimiento y calcula cuántos años han pasado desde esa fecha hasta hoy.  
Permite reutilizar esta lógica en cualquier parte del HTML de forma limpia, legible y reutilizable.

---

## 🧠 Conceptos aplicados

- Creación de pipes personalizados en Angular
- Uso de `PipeTransform` para transformar datos
- Manipulación de fechas con `Date`
- Cálculo de edad en base a fecha de nacimiento

---

## 💡 Variaciones sugeridas

### ✅ 1. Mostrar edad con texto adicional

```html
<p>Tienes aproximadamente {{ '1985-09-01' | edad }} años de experiencia.</p>
```

📌 **¿Por qué?**: Puedes integrar el pipe directamente dentro de frases y contenido del template.

---

### ✅ 2. Validar entrada vacía o inválida

```ts
transform(fechaNacimiento: string | Date): number | string {
  if (!fechaNacimiento) return 'Fecha no válida';
  // resto del cálculo...
}
```

📌 **¿Por qué?**: Mejora la robustez ante entradas incorrectas o vacías.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Carga el componente y observa el número mostrado.
2. Cambia la fecha de nacimiento en el HTML y comprueba que se actualiza la edad.
3. Prueba introducir una fecha inválida o vacía y asegúrate de que el pipe lo gestiona correctamente si has hecho la variación 2.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](./Ejemplo_4.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 8](../../Modulo_8.md)

### 🏠 - [Inicio](../../../README.md)

