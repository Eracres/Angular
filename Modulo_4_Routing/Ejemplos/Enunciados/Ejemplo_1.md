# 🧪 Ejemplo 1: Configuración básica del Router

## `app-routing.module.ts`
```ts
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { InicioComponent } from './inicio/inicio.component';
import { AcercaComponent } from './acerca/acerca.component';

const routes: Routes = [
  { path: '', component: InicioComponent },
  { path: 'acerca', component: AcercaComponent }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

## ✅ ¿Qué hace este componente?
Este módulo configura las rutas iniciales de la aplicación: la raíz (`''`) y `/acerca`.

---

## 🧠 Conceptos aplicados
- Definición de rutas con `Routes`
- Importación de `RouterModule`
- Uso de `forRoot()`


---

## 💡 Variaciones sugeridas
```ts
Agregar una ruta extra para `/contacto`
```
```ts
Crear una ruta por defecto para redirección
```


---

## 🔁 Navegación

### 🧪 - Ejemplo 2 [➡️](./Ejemplo_2.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 [Volver a Módulo 4](../../Modulo_4.md)

### 🏠 [Inicio](../../../README.md)
