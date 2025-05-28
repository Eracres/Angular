# 🧪 Ejemplo 6: Uso de servicio con ngOnInit

## `login.service.ts`
```ts
@Injectable({ providedIn: 'root' })
export class LoginService {
  logueado = false;

  login() {
    this.logueado = true;
  }

  logout() {
    this.logueado = false;
  }

  estaLogueado() {
    return this.logueado;
  }
}
```

## `header.component.ts`
```ts
@Component({...})
export class HeaderComponent implements OnInit {
  logueado = false;

  constructor(private loginService: LoginService) {}

  ngOnInit() {
    this.logueado = this.loginService.estaLogueado();
  }
}
```

## ✅ ¿Qué hace este componente?
Consulta el estado del login al inicializarse, accediendo a un servicio.

---

## 🧠 Conceptos aplicados
- Encapsulamiento de estado global
- Uso de ngOnInit
- Consulta de flags booleanos

---

## 💡 Variaciones sugeridas
```ts
Mostrar nombre del usuario logueado
```

---
## 🔁 Navegación

### 🧪 - [⬅️](./Ejemplo_5.md) Ejemplo 5 - Modulo 6 [➡️](../../../Modulo_6_Formularios_y_Validaciones/Modulo_6.md)

### 🧪 - [Volver a Ejemplos](../README.md)

### 📋 - [Ir a Ejercicios](../../Ejercicios/README.md)

### 📘 - [Volver a Módulo 5](../../Modulo_5.md)

### 🏠 - [Inicio](../../../README.md)
