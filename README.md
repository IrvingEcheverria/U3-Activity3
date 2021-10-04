# U3-Activity3

/*
// USE  STRICT

// 1. Evitar creación de Variables Globales Accidentales.
{
    'use strict';
let nombre = 'Irving';
let edad = 29;

if (edad > 20) {
    nmbre = 'Gessu'; // Al usar use strict aparecerá: nmbre is not defined ...
    // y evitará que se cree una Var Global.
}}


// 2. Cambiar Atributos de solo Lectura.
{
    'use strict'; // Al usarla no permitirá asignar un nuevo Valor (Gessu) a la Propiedad (Nombre) de Solo Lectura.
    const usuario = {};
    Object.defineProperty(usuario, 'nombre', { value: 'Irving', writable: false });

    usuario.nombre = 'Gessu';
    console.log(usuario.nombre);

}


// 3. Objetos no extensiles
{
    'use strict'; // Si no se usa, No marcará error... a pesar de que prevent cumple su función.
    // Si se usa marcará error: No se puede agregar propiedad a un objeto no extensible.
    const usuario = { nombre: 'Irving' };
    Object.preventExtensions(usuario); // .preventExtension previene agregar Propiedades a un objeto...
    // Si lo comentamos object.prevent... agregará la propiedad Edad.

    usuario.edad = 29;
    console.log(usuario);
}

{
    'use strict';
    let nombre = 'Irving'
    nombre.modificado = false;
    console.log(nombre.modificado);
    // En modo estricto no permitirá agregar una Propiedad (Modificado) a un Valor primitivo (como String).
}


// 4. Parámetros duplicados //
{
    'use strict'; // Notificará el error de duplicación...
    // Al no usarlo e invocar la función, aparecerá Undefined pues tomará el último "nombre" pero sin tener un tercer Valor).
    function saludar(nombre, apellido, nombre) {
        console.log(`Hola ${nombre} ${apellido}`)
    }
    saludar('Irving', 'Echverría') // Se está llamado a una función de 3var pero con solo 2 Valores).
}


// 5. SISTEMA OCTAL (Sistema con base 8, representa numero con digitos del 0 al 7).
{
    // 'use strict';
    console.log(011); // 9 = 1 + 1*8
    console.log(023); // 19 = 3 + 2*8

    // Al usar modo estricto deberás poner una o (mayus o minus) entre el 0 y segund dígito para poder escribir en octal.
    // Ejemplo: (0o11) y (0o23).
}

// 6. ERRORES CON DELETE
{
    function saludar() {
        console.log('Hola');
    }
    const nombre = 'Irving';

    'use strict';
delete nombre; // Strict modo nos indicará con un error si una Propiedad no se puede borrar.
delete saludar;
delete windows;
}

// 7. EVAL & ARGUMENTS:
{
    'use strict'; // Strict evitará que se usen ambas palabras como nombre de variables.
    let eval = 'x valor';
    let arguments = 'y valor';
}

// 8. NO SE PERMITE LA FUNCIÓN "WITH": Esta sirve para extener la cadena de scopes de JS temporalmente.
{
'use strict'; 7/ Strict mode no incluirá esa instrucción.

with (document.forms[0]) {
email.value = '';
password.value ='';
}

// Es mejor guardar una referencia (Ej: "Form") del objeto:
const form = document.forms[0]
form.email.value = '';
form.password.value = '';
}

// 9. PALABRAS RESERVADAS: class enum extends super const export import
{
    'use strict';
    let package = 'paquete 1'; // Indicará error pues Package es una palabra reservada en modo estricto.
    // Otras palabras son: implements interface protected package static yield public private & let
}

// 10. FUNCIONES LIBRES
{
    'use strict';

    const usuario = {
        nombre: 'Irving',
        saludar: function () {
            consle.log(`Hola, soy ${this.nombre}`);
            }
    }

    // usuario.saludar(); // cuando se ejecuta sin strict mode this llamará al valor de la propiedad del nombre.
const saludar = usuario.saludar;
saludar(); // sin modo strict llamarla de este modo la llamará de modo global, no tendrá valor la propiedad e indicará error de Undefined.
// En modo stric, llamarla de esa manera no tendrá dueño global y marcará inmediatamente error.
}

*/
