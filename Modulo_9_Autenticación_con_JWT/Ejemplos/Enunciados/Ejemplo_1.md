# 🧪 Ejemplo 1: Crear servicio AuthService

## 🎯 Objetivo
Implementar un servicio de autenticación (`AuthService`) que gestione el inicio de sesión y el almacenamiento del token JWT simulado.

## 📁 Ruta: src/app/auth.service.ts
```ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class AuthService {
  private tokenKey = 'token';

  login(email: string, password: string): void {
    if (email && password) {
      localStorage.setItem(this.tokenKey, 'falso-token');
    }
  }

  logout(): void {
    localStorage.removeItem(this.tokenKey);
  }

  estaAutenticado(): boolean {
    return !!localStorage.getItem(this.tokenKey);
  }
}
```

---

## ✅ ¿Qué hace este componente?
El servicio `AuthService` simula el comportamiento de un sistema de autenticación:

- Al llamar a `login()`, guarda un token falso en `localStorage`.
- `logout()` elimina ese token.
- `estaAutenticado()` comprueba si el token existe, indicando si el usuario está autenticado.

---

## 🧠 Conceptos aplicados

- Servicios Angular (`@Injectable`)
- Almacenamiento local (`localStorage`)
- Simulación de flujos de autenticación
- Reutilización de lógica de seguridad en toda la app

---

## 💡 Variaciones sugeridas

### ✅ 1. Guardar el email del usuario en localStorage

```ts
login(email: string, password: string): void {
  if (email && password) {
    localStorage.setItem(this.tokenKey, 'falso-token');
    localStorage.setItem('email', email);
  }
}
```

📌 **¿Por qué?**: Permite mostrar el nombre del usuario logueado en la interfaz.

---

### ✅ 2. Verificar token al iniciar la app

```ts
ngOnInit() {
  const logueado = this.authService.estaAutenticado();
  if (logueado) {
    // Redirigir al dashboard o mostrar usuario
  }
}
```

📌 **¿Por qué?**: Mejora la UX validando la sesión desde el principio.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Llama a `authService.login('test', '123')` y revisa `localStorage`.
2. Usa `authService.estaAutenticado()` para validar si devuelve `true`.
3. Llama a `authService.logout()` y asegúrate de que se borre el token.

---

## 🔁 Navegación

### 🧪 - Ejemplo 2 [➡️](./Ejemplo_2.md)
### 🧪 - [Volver a Ejemplos](../README.md)
### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)
### 📘 - [Volver a Módulo 9](../../Modulo_9.md)
### 🏠 - [Inicio](../../../README.md)

