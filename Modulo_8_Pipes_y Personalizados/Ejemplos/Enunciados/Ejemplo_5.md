# 🧪 Ejemplo 5: Pipe personalizado calcularEdad

## 🎯 Objetivo
Crear un pipe que calcule automáticamente la edad de una persona a partir de su fecha de nacimiento.

---

## 📁 Ruta: src/app/pipes/calcular-edad.pipe.ts
```ts
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({ name: 'calcularEdad' })
export class CalcularEdadPipe implements PipeTransform {
  transform(fechaNacimiento: string): number {
    const hoy = new Date();
    const nacimiento = new Date(fechaNacimiento);
    let edad = hoy.getFullYear() - nacimiento.getFullYear();
    const mes = hoy.getMonth() - nacimiento.getMonth();

    if (mes < 0 || (mes === 0 && hoy.getDate() < nacimiento.getDate())) {
      edad--;
    }

    return edad;
  }
}
```

---

## 📁 Ruta: src/app/app.component.ts
```ts
export class AppComponent {
  fechaNacimiento = '1990-06-15';
}
```

---

## 📁 Ruta: src/app/app.component.html
```html
<p>Edad: {{ fechaNacimiento | calcularEdad }}</p>
```

---

## ✅ ¿Qué hace este ejemplo?

Este ejemplo implementa un pipe personalizado llamado `calcularEdad`, que recibe una fecha en formato string y devuelve la edad actual calculada a partir de dicha fecha.

Es útil para mostrar automáticamente la edad de una persona sin necesidad de actualizarla manualmente.

---

## 🧠 Conceptos aplicados

- Creación de pipes personalizados
- Uso de lógica de fecha con `Date`
- Transformación de datos en plantillas
- Aplicación de `PipeTransform`

---

## 💡 Variaciones sugeridas

### ✅ 1. Mostrar la edad como string con “años”

```ts
return `${edad} años`;
```

📌 ¿Por qué?: Mejora la presentación del resultado en la interfaz.

---

### ✅ 2. Permitir fechas en diferentes formatos

```ts
const nacimiento = new Date(Date.parse(fechaNacimiento));
```

📌 ¿Por qué?: Permite una mayor flexibilidad con formatos de entrada.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Asegúrate de que el pipe esté declarado en el módulo.
2. Cambia el valor de `fechaNacimiento` y verifica que la edad calculada cambia correctamente.
3. Prueba con fechas recientes y antiguas para comprobar la precisión.
4. Usa el pipe en diferentes partes de la app para reutilizarlo.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](./Ejemplo_6.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 8](../../Modulo_8_Pipes_y_Personalizados.md)

### 🏠 - [Inicio](../../../README.md)
