[# LEEEME - SpawnCamp
](https://jddz-code.github.io/A3_Projecte_Fase_2_botiga/)
## Catálogo y buscador

El catálogo se genera en Js/catalogo.js.

La función crearTarjeta construye cada tarjeta con el DOM (createElement, textContent y appendChild), mostrarJuegos las pinta en la página y calculaPrecioConIva calcula el precio con IVA.

El buscador y el filtro por plataforma están en el mismo archivo, en la función filtrarJuegos. Esa función también actualiza el texto "Mostrando X de Y juegos".

## Formulario de contacto

El formulario está en Js/contacto.js.

La función validarFormulario comprueba los campos, mostrarError y borrarErrores gestionan los avisos de error, quitarErrorCampo los quita cuando el usuario corrige, actualizarContador cuenta los caracteres del mensaje y mostrarResumen crea la tarjeta de confirmación.

## Modo claro y oscuro

Está en Js/tema.js.

La función aplicarTema activa o quita la clase modo-claro en el body con classList.toggle, cambia el texto del botón y guarda la elección en localStorage para que el tema se mantenga al cambiar de página. La función obtenerTemaGuardado recupera esa elección al cargar la página. Si no hay nada guardado, la web arranca en modo oscuro.

Los colores de los dos modos están en Css/style.css.

## const o let

En validarFormulario uso let todoCorrecto = true porque su valor cambia a false cuando algún campo está mal. El resto de variables son const porque nunca se reasignan.

## Callback

validarFormulario se pasa a addEventListener("submit", ...) y se ejecuta cuando el usuario pulsa "Enviar", para validar los datos y mostrar los errores o el resumen.

## Arrow function

En filtrarJuegos uso juegos.filter((juego) => ...), que devuelve true si el título y la plataforma del juego coinciden con lo que se ha buscado.
