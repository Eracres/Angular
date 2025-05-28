# 🧪 Ejemplo 3: Servicio compartido entre componentes

## `contador.service.ts`
```ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class ContadorService {
  valor = 0;

  incrementar() {
    this.valor++;
  }

  obtenerValor() {
    return this.valor;
  }
}
```

## `boton.component.ts`
```ts
@Component({...})
export class BotonComponent {
  constructor(private contador: ContadorService) {}

  incrementar() {
    this.contador.incrementar();
  }
}
```

## `resultado.component.ts`
```ts
@Component({...})
export class ResultadoComponent {
  constructor(public contador: ContadorService) {}
}
```

## ✅ ¿Qué hace este componente?
Comparte una instancia de servicio entre dos componentes independientes.

---

## 🧠 Conceptos aplicados
- Singleton por defecto en servicios Angular
- Compartir estado
- Comunicación sin @Input/@Output

---

## 💡 Variaciones sugeridas
```ts
Agregar método para reiniciar contador
```

---
## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](./Ejemplo_4.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 5](../../Modulo_5.md)

### 🏠 - [Inicio](../../../README.md)

