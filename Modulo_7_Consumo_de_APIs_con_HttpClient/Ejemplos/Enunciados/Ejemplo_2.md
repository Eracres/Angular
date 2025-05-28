# 🧪 Ejemplo 2: Servicio básico con GET

## `app.module.ts`
```ts
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { HttpClientModule } from '@angular/common/http';
import { AppComponent } from './app.component';

@NgModule({
  declarations: [AppComponent],
  imports: [BrowserModule, HttpClientModule],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

## ✅ ¿Qué hace este ejemplo?
Este ejemplo demuestra cómo importar `HttpClientModule` en el módulo principal de Angular para poder usar servicios HTTP en la aplicación.

---

## 🧠 Conceptos aplicados
- Importación de módulos en Angular
- Activación de `HttpClient` a nivel global
- Configuración base para consumo de APIs

---


## 💡 Variaciones sugeridas

### 🔹 Importar `HttpClientModule` en un módulo secundario

```ts
// user.module.ts
import { NgModule } from '@angular/core';
import { CommonModule } from '@angular/common';
import { HttpClientModule } from '@angular/common/http';

@NgModule({
  imports: [CommonModule, HttpClientModule]
})
export class UserModule {}
```

### 🔹 Añadir un interceptor HTTP para token de autenticación

```ts
// token.interceptor.ts
import { Injectable } from '@angular/core';
import { HttpInterceptor, HttpRequest, HttpHandler } from '@angular/common/http';

@Injectable()
export class TokenInterceptor implements HttpInterceptor {
  intercept(req: HttpRequest<any>, next: HttpHandler) {
    const tokenizedReq = req.clone({
      setHeaders: { Authorization: `Bearer TU_TOKEN` }
    });
    return next.handle(tokenizedReq);
  }
}
```

```ts
// app.module.ts
import { HTTP_INTERCEPTORS } from '@angular/common/http';
import { TokenInterceptor } from './token.interceptor';

@NgModule({
  providers: [
    { provide: HTTP_INTERCEPTORS, useClass: TokenInterceptor, multi: true }
  ]
})
export class AppModule {}
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](./Ejemplo_3.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 7](../../Modulo_7.md)

### 🏠 - [Inicio](../../../README.md)


