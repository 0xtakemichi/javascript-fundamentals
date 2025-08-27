# Variables en JavaScript

En JavaScript existen 3 formas de declarar variables `var`, `let` y `const`.

### Var
Era la forma inicial que habia de delcarar variables, hoy en día está obsoleta.

### Let
Es reasignable solo dentro del bloque de ejecución

### Const
Es inmutable, no puede ser reasignada

### Scope (Alcance)
```
if (true) {
    var a = 'var dentro de if' // Disponible fuera del bloque
    let b = 'let dentro de if' // Solo disponible dentro del bloque
    const c = 'const dentro de if' // Solo disponible dentro del bloque
}
console.log(a) // Funciona
// console.log(b) // Error: b no está definida
// console.log(c) // Error: c no está definida