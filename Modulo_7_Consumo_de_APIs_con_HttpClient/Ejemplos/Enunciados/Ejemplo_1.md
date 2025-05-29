# 🧪 Ejemplo 1: Importación de HttpClientModule

## 📁 Ruta: src/app/app.module.ts

```ts
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { AppComponent } from './app.component';
import { HttpClientModule } from '@angular/common/http';

@NgModule({
  declarations: [AppComponent],
  imports: [
    BrowserModule,
    HttpClientModule // Importación clave para trabajar con APIs
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

---

## ✅ ¿Qué hace este ejemplo?

Este ejemplo muestra cómo **habilitar el módulo `HttpClientModule`** de Angular para poder hacer peticiones HTTP.  
Sin esta importación, **no se pueden consumir APIs REST** en Angular.

- Angular no activa el servicio `HttpClient` por defecto, por lo que **es obligatorio importar** `HttpClientModule` dentro del `@NgModule` principal (normalmente en `app.module.ts`).
- Una vez hecho esto, cualquier servicio de la aplicación podrá inyectar `HttpClient` y usarlo para peticiones GET, POST, PUT, DELETE, etc.

---

## 🧠 Conceptos aplicados

- Importación de módulos externos en Angular
- Habilitación del cliente HTTP de Angular (`HttpClient`)
- Estructura del `AppModule` y su función de configuración

---

## 💡 Variaciones sugeridas

### ✅ 1. Importar `HttpClientModule` en un módulo de características

📁 Ruta: src/app/otro-modulo/otro-modulo.module.ts

```ts
// Si tienes un módulo exclusivo para usuarios
import { HttpClientModule } from '@angular/common/http';

@NgModule({
  imports: [HttpClientModule]
})
export class UsuarioModule { }
```
📌 **¿Por qué?**: Ideal para mantener el proyecto modularizado. Solo cargas `HttpClient` donde se necesita.

---

### ✅ 2. Usar `HttpClientModule` junto a interceptores HTTP

📁 Ruta: src/app/interceptors/auth.interceptor.ts

```ts
import { HTTP_INTERCEPTORS } from '@angular/common/http';
import { MiInterceptor } from './interceptores/mi-interceptor';

@NgModule({
  providers: [
    {
      provide: HTTP_INTERCEPTORS,
      useClass: MiInterceptor,
      multi: true
    }
  ]
})
export class AppModule { }
```
📌 **¿Por qué?**: Los interceptores permiten modificar todas las peticiones o respuestas HTTP (por ejemplo, para agregar tokens JWT o manejar errores globalmente).

---

## 🔁 Navegación

### 🧪 - Ejemplo 2 [➡️](./Ejemplo_2.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 7](../../Modulo_7.md)

### 🏠 - [Inicio](../../../README.md)

