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

```ts
// Importar HttpClientModule en un módulo específico en vez del AppModule
```

```ts
// Usar HttpClientModule en combinación con interceptores
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](./Ejemplo_3.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 7](../../Modulo_7.md)

### 🏠 - [Inicio](../../../README.md)

