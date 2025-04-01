# Curso Completo de Angular – Desarrollo de Aplicaciones Web

Este curso está diseñado para llevarte paso a paso desde cero hasta construir y desplegar aplicaciones web modernas usando Angular. A continuación encontrarás todos los módulos explicados en detalle, con ejemplos prácticos y ejercicios para afianzar lo aprendido.

---

## 📦 MÓDULO 1: Introducción a Angular

### ✅ ¿Qué es Angular?
Angular es un framework frontend desarrollado por Google para construir aplicaciones web de una sola página (SPA). Está basado en TypeScript y ofrece herramientas integradas para componentes, formularios, routing, HTTP, servicios, inyección de dependencias, entre otros.

### ✅ Instalación del entorno
1. Instala [Node.js](https://nodejs.org)
2. Instala Angular CLI:
```bash
npm install -g @angular/cli
```
3. Crea un proyecto:
```bash
ng new hola-angular
cd hola-angular
ng serve
```

### ✅ Estructura del proyecto
- `src/app/app.component.ts`: Lógica del componente principal
- `src/app/app.component.html`: Vista
- `src/app/app.module.ts`: Módulo raíz

### ✅ Crear un componente
```bash
ng generate component saludo
```

```ts
export class SaludoComponent {
  nombre: string = 'Estudiante';
}
```

```html
<h2>Hola, {{ nombre }} 👋</h2>
```

**Ejercicio:** Crear un componente `bienvenida` que muestre un saludo personalizado.

---

## 🧩 MÓDULO 2: Componentes y Data Binding

### ✅ Tipos de Enlace de Datos
- Interpolación: `{{ variable }}`
- Property binding: `[src]="imagen"`
- Event binding: `(click)="accion()"`
- Two-way binding: `[(ngModel)]="valor"`

### ✅ Uso de `FormsModule`
```ts
import { FormsModule } from '@angular/forms';
```

### ✅ Ejemplo completo
```ts
nombre = 'Laptop Gamer';
precio = 1500;
mostrarInfo() {
  alert(`Producto: ${this.nombre}`);
}
```

```html
<h3>{{ nombre }}</h3>
<p>{{ precio }}</p>
<button (click)="mostrarInfo()">Ver detalles</button>
```

**Ejercicio:** Componente `usuario` editable con `[(ngModel)]` y botón con `alert`.

---

## 🧭 MÓDULO 3: Directivas Angular

### ✅ Estructurales
- `*ngIf`, `*ngFor`, `*ngSwitch`

```html
<p *ngIf="mostrar">Visible</p>
<li *ngFor="let item of lista">{{ item }}</li>
```

### ✅ De atributo
- `ngClass`, `ngStyle`

```html
<p [ngClass]="{ 'verde': activo }"></p>
```

**Ejercicio:** Componente `carrito` con condicionales y estilo dinámico.

---

## 🔀 MÓDULO 4: Routing

### ✅ Configuración
```ts
const routes: Routes = [
  { path: '', component: InicioComponent },
  { path: 'acerca', component: AcercaComponent }
];
```

### ✅ Uso de `<router-outlet>` y `routerLink`
```html
<a routerLink="/acerca">Acerca</a>
<router-outlet></router-outlet>
```

**Ejercicio:** Crear navegación entre `/`, `/servicios`, `/contacto` y página 404.

---

## 🛠️ MÓDULO 5: Servicios y Comunicación

### ✅ Crear servicio
```bash
ng generate service servicios/producto
```

```ts
export class ProductoService {
  productos = [...];
  obtenerProductos() {
    return this.productos;
  }
}
```

**Ejercicio:** Crear `carrito.service.ts` y compartirlo entre dos componentes.

---

## 📝 MÓDULO 6: Formularios y Validaciones

### ✅ Template-driven forms
```html
<form (ngSubmit)="enviar()">
  <input [(ngModel)]="nombre" name="nombre" required>
</form>
```

### ✅ Validaciones básicas
```html
<div *ngIf="campo.errors?.required">Campo obligatorio</div>
```

**Ejercicio:** Componente `registro-usuario` con nombre, email, contraseña.

---

## 🌐 MÓDULO 7: Consumo de APIs con HttpClient

### ✅ Configuración
```ts
import { HttpClientModule } from '@angular/common/http';
```

### ✅ Servicio de API
```ts
getUsuarios() {
  return this.http.get('https://jsonplaceholder.typicode.com/users');
}
```

**Ejercicio:** Componente `usuarios` que consuma y muestre datos.

---

## 🧪 MÓDULO 8: Pipes y Personalizados

### ✅ Pipes comunes
- `uppercase`, `currency`, `date`, `json`

### ✅ Crear pipe personalizado
```ts
@Pipe({ name: 'descuento' })
export class DescuentoPipe implements PipeTransform {
  transform(valor: number, porcentaje: number) {
    return valor - (valor * porcentaje / 100);
  }
}
```

**Ejercicio:** Crear `mayusInvertido` y `calcularEdad`.

---

## 🔐 MÓDULO 9: Autenticación con JWT

### ✅ AuthService
```ts
login(email, password) {
  localStorage.setItem('token', 'falso-token');
}
```

### ✅ AuthGuard
```ts
canActivate(): boolean {
  return this.auth.estaAutenticado();
}
```

**Ejercicio:** Crear login simulado y proteger `/dashboard`.

---

## 🚀 MÓDULO 10: Despliegue

### ✅ Compilar app
```bash
ng build --configuration production
```

### ✅ Firebase
```bash
firebase init
firebase deploy
```

### ✅ Netlify o Vercel
Subir carpeta `dist/` o usar CLI de `vercel`.

**Tarea final:** Publicar tu app y compartir URL.

---

## 💼 Proyecto Integrador: Sistema de Gestión de Productos

### ✅ Características
- Login con JWT simulado
- Dashboard protegido
- CRUD de productos
- Validaciones + Pipes personalizados
- API simulada con JSON Server
- Despliegue en Firebase o Netlify

---

¡Felicidades! Has completado el curso completo de Angular 🎉

