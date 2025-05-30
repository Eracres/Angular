# 📘 Módulo 8: Pipes y creación de Pipes personalizados

## ❓ ¿Qué es un Pipe?

Los **pipes** en Angular son funciones que permiten **transformar valores directamente en la plantilla HTML**. Son útiles para formatear textos, fechas, monedas, porcentajes, entre otros.

Angular incluye pipes comunes predefinidos, pero también puedes crear los tuyos propios.

---

## 🛠️ Pipes comunes de Angular

| Pipe         | Uso en plantilla              | Ejemplo salida           |
|--------------|-------------------------------|--------------------------|
| `uppercase`  | `{{ 'hola' | uppercase }}`     | `HOLA`                   |
| `lowercase`  | `{{ 'ANGULAR' | lowercase }}`  | `angular`                |
| `titlecase`  | `{{ 'curso angular' | titlecase }}` | `Curso Angular`     |
| `date`       | `{{ fecha | date:'dd/MM/yyyy' }}` | `29/05/2025`         |
| `currency`   | `{{ precio | currency:'EUR' }}` | `120,00 €`             |
| `json`       | `{{ objeto | json }}`          | `{"nombre": "Juan"}`     |

---

## ✏️ Crear un Pipe personalizado

Para crear un pipe se debe:

1. Usar el decorador `@Pipe`.
2. Implementar la interfaz `PipeTransform`.
3. Registrar el pipe en un módulo.

### 📁 Ruta: src/app/pipes/descuento.pipe.ts

```ts
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({ name: 'descuento' })
export class DescuentoPipe implements PipeTransform {
  transform(valor: number, porcentaje: number): number {
    return valor - (valor * porcentaje / 100);
  }
}
```

📌 En el HTML: `{{ 100 | descuento:20 }}` → `80`

---

## 🧠 Conceptos clave aplicados

- Uso de pipes como transformadores de salida en plantillas
- Uso de pipes encadenados: `{{ valor | currency | uppercase }}`
- Pipes con parámetros adicionales
- Definición y aplicación de pipes personalizados
- Separación entre lógica de presentación y lógica de negocio

---

## 💡 Pipes personalizados sugeridos

### ✅ 1. Pipe `mayusInvertido`

📁 Ruta: src/app/pipes/mayus-invertido.pipe.ts

```ts
@Pipe({ name: 'mayusInvertido' })
export class MayusInvertidoPipe implements PipeTransform {
  transform(valor: string): string {
    return valor.split('').reverse().join('').toUpperCase();
  }
}
```

📌 `{{ 'angular' | mayusInvertido }}` → `RALUGNA`

---

### ✅ 2. Pipe `calcularEdad`

📁 Ruta: src/app/pipes/calcular-edad.pipe.ts

```ts
@Pipe({ name: 'calcularEdad' })
export class CalcularEdadPipe implements PipeTransform {
  transform(fechaNacimiento: string): number {
    const nacimiento = new Date(fechaNacimiento);
    const hoy = new Date();
    let edad = hoy.getFullYear() - nacimiento.getFullYear();
    const m = hoy.getMonth() - nacimiento.getMonth();
    if (m < 0 || (m === 0 && hoy.getDate() < nacimiento.getDate())) {
      edad--;
    }
    return edad;
  }
}
```

📌 `{{ '1990-04-01' | calcularEdad }}` → `35`

---

## ✅ ¿Cómo verificar que funcionan correctamente?

1. Declara tus pipes en el `declarations` del módulo correspondiente.
2. Úsalos en la plantilla HTML con la sintaxis `{{ valor | pipePersonalizado }}`
3. Prueba valores distintos y asegúrate de que el resultado es correcto.
4. En pipes con parámetros, verifica distintos casos de entrada.

---

## 🧪 Ejemplos de este módulo

#### [🔗 Listado de Ejemplos](./Ejemplos/README.md)

---

## 📋 Ejercicios propuestos

#### [🔗 Listado de Ejercicios](./Ejercicios/README.md)

---

## 🔁 Navegación

### [⬅️](../Modulo_7_Consumo_APIs_HttpClient/Modulo_7.md) Módulo 7 - Módulo 9 [➡️](../Modulo_9.md)

### 🏠 [Inicio](../README.md)
