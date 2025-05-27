# 🧪 Ejemplo 6: Redirección de rutas

## `app-routing.module.ts`
```ts
const routes: Routes = [
  { path: '', redirectTo: '/inicio', pathMatch: 'full' },
  { path: 'inicio', component: InicioComponent }
];
```

## ✅ ¿Qué hace este componente?
Esta configuración redirige automáticamente la ruta raíz (`''`) hacia `/inicio`.

---

## 🧠 Conceptos aplicados
- Redirección de rutas
- Uso de `redirectTo`
- Importancia de `pathMatch: 'full'`


---

## 💡 Variaciones sugeridas
```ts
Redirigir otras rutas como `/home` → `/inicio`
```
```ts
Combinar redirección con rutas hijas
```

---

## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_5.md) Ejemplo 5 - Modulo 4 [➡️](../../../Modulo_4_Routing/Modulo_4.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 4](../../Modulo_4.md)

### 🏠 - [Inicio](../../../README.md)

