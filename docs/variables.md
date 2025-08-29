# Variables en JavaScript

En JavaScript existen 3 formas de declarar variables `var`, `let` y `const`.

### Var
Fue la forma inicial que habia de declarar variables. Hoy en día está obsoleta y no se recomienda su uso en código moderno.

Características:
- Scope de función o global.
- Puede ser redeclarada.
- Sufre de hoisting.

```javascript
var nombre = "Pepe";
var nombre = "David";
```

### Let
Introducida en ES6, permite que las variables sean reasignadas, pero solo dentro del bloque en el que fueron definidas.

Características:
- Tiene scope de bloque.
- No puede ser redeclarada en el mismo scope.
- Sí puede ser reasignada

```javascript
let edad = 20;
edad = 30;
let edad = 18; // ❌
if (true) {
    let edad = 24; // ✅
}
```

### Const
Introducida en ES6, se utiliza para valores que no deben cambiar.

Características:
- Scope de bloque
- No puede ser redeclarada
- No puede ser reasignada
- Debe inicializarse al declararla

```javascript
const PI = 3.1416;
PI = 3.1515; // ❌
```

## Conceptos Clave

### Scope (Alcance)
El scope se refiere al contexto donde una variable es accesible.

```javascript
if (true) {
    var a = 'var dentro de if' // Disponible fuera del bloque
    let b = 'let dentro de if' // Solo disponible dentro del bloque
    const c = 'const dentro de if' // Solo disponible dentro del bloque
}
console.log(a) // Funciona
console.log(b) // Error: b no está definida
console.log(c) // Error: c no está definida
```

### Hoisting
JavaScript "eleva" las declaraciones de variables al top de su scope.

```javascript
console.log(x) // undefined (pero no error)
var x = 5;

console.log(y) // ❌ Error: Cannot access 'y' before initialization
let y = 10;

console.log(z) // ❌ Error: Cannot access 'z' before initialization
const z = 15;
```

### Buenas Prácticas
1. Usar `const` para todos los valores que no cambien
2. Usar `let` cuando se necesite reasignar valores
3. Evitar `var` en código moderno
4. Nombres descriptivos para mejor legibilidad

### Convenciones de nombres de variables
Existen diferentes convenciones de nombres para declarar variables en programación, ya que esto hace que el código sea más legible y consistente.

En JavaScript es más común utilizar lowerCamelCase, donde la primera palabra empieza en minúscula y cada palabra siguiente inicia con mayúscula.

- lowerCamelCase -> myName
- Snake_case -> my_name.
- PascalCase -> MyName.
- Kebab-case -> my-name.