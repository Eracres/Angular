# 🧪 Ejemplo 2: Servicio de autenticación básico

## 🎯 Objetivo
Crear un servicio que gestione la autenticación de usuarios simulando el uso de JWT (token almacenado localmente).

## 📁 Ruta: src/app/auth.service.ts
```ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class AuthService {
  login(email: string, password: string): void {
    if (email && password) {
      localStorage.setItem('token', 'falso-token');
    }
  }

  logout(): void {
    localStorage.removeItem('token');
  }

  estaAutenticado(): boolean {
    return !!localStorage.getItem('token');
  }
}
```

---

## ✅ ¿Qué hace este ejemplo?

Este servicio `AuthService` permite simular un inicio de sesión muy básico usando el almacenamiento local para guardar un "token".  
Incluye métodos para iniciar sesión (`login`), cerrar sesión (`logout`) y verificar si el usuario está autenticado (`estaAutenticado`).

---

## 🧠 Conceptos aplicados

- Almacenamiento en `localStorage`
- Simulación de login y logout
- Servicios inyectables y reutilizables
- Control de estado autenticado

---

## 💡 Variaciones sugeridas

### ✅ Añadir retorno booleano al login

```ts
login(email: string, password: string): boolean {
  if (email === 'admin@test.com' && password === '1234') {
    localStorage.setItem('token', 'token-valido');
    return true;
  }
  return false;
}
```

📌 **¿Por qué?**: Permite mostrar mensajes o redirigir según éxito o fallo.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Inyecta `AuthService` en el componente de login.
2. Llama a `login()` con un email y contraseña simulada.
3. Comprueba que `localStorage.getItem('token')` devuelve el valor esperado.
4. Llama a `logout()` y verifica que el token se elimina correctamente.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](./Ejemplo_3.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 9](../../Modulo_9.md)

### 🏠 - [Inicio](../../../README.md)

