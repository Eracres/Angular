# 🧪 Ejemplo 3: Crear un AuthGuard para proteger rutas

## 🎯 Objetivo
Proteger rutas específicas en la aplicación usando un guard de autenticación (`AuthGuard`) que valide si el usuario está autenticado.

## 📁 Ruta: src/app/auth.guard.ts
```ts
import { Injectable } from '@angular/core';
import { CanActivate, Router } from '@angular/router';
import { AuthService } from './auth.service';

@Injectable({
  providedIn: 'root'
})
export class AuthGuard implements CanActivate {
  constructor(private auth: AuthService, private router: Router) {}

  canActivate(): boolean {
    if (this.auth.estaAutenticado()) {
      return true;
    } else {
      this.router.navigate(['/login']);
      return false;
    }
  }
}
```

---

## ✅ ¿Qué hace este ejemplo?

Este ejemplo crea un **AuthGuard** que se encarga de verificar si el usuario está autenticado antes de acceder a ciertas rutas.  
Si no lo está, redirige al usuario a la página de login.

---

## 🧠 Conceptos aplicados

- Uso de interfaces como `CanActivate` en Angular
- Redirección con `Router`
- Inyección de servicios
- Seguridad en navegación por rutas

---

## 💡 Variaciones sugeridas

### ✅ Aplicar el guard en una ruta protegida

```ts
const routes: Routes = [
  { path: 'dashboard', component: DashboardComponent, canActivate: [AuthGuard] }
];
```
📌 **¿Por qué?**: Para restringir acceso solo a usuarios autenticados.

---

## ✅ ¿Cómo verificar que funciona correctamente?

1. Define una ruta con `canActivate: [AuthGuard]`.
2. Intenta acceder a esa ruta sin iniciar sesión y asegúrate de ser redirigido.
3. Haz que `estaAutenticado()` devuelva `true` y verifica que ahora sí puedes entrar.

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](./Ejemplo_4.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 9](../../Modulo_9.md)

### 🏠 - [Inicio](../../../README.md)

