# 🧪 Ejemplo 5: Servicio con arreglo dinámico

## `mensaje.service.ts`
```ts
@Injectable({ providedIn: 'root' })
export class MensajeService {
  mensajes: string[] = [];

  agregar(mensaje: string) {
    this.mensajes.push(mensaje);
  }

  limpiar() {
    this.mensajes = [];
  }
}
```

## ✅ ¿Qué hace este servicio?
Permite registrar mensajes y luego consultarlos desde distintos componentes.

---

## 🧠 Conceptos aplicados
- Servicio con lógica dinámica
- Uso en múltiples vistas
- Arreglo como contenedor de estado

---

## 💡 Variaciones sugeridas
```ts
Agregar timestamps a los mensajes
```

---
## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](./Ejemplo_6.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 5](../../Modulo_5.md)

### 🏠 - [Inicio](../../../README.md)
