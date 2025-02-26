---
title: Promise.reject()
slug: Web/JavaScript/Reference/Global_Objects/Promise/reject
translation_of: Web/JavaScript/Reference/Global_Objects/Promise/reject
original_slug: Web/JavaScript/Referencia/Objetos_globales/Promise/reject
---
{{JSRef}}

El método **`Promise.reject(reason)`** retorna un objeto `Promise` que es rechazado por la razón específicada.

{{EmbedInteractiveExample("pages/js/promise-reject.html")}}

## Sintaxis

```
Promise.reject(reason);
```

### Parámetros

- reason
  - : Razón por la cual esta {jsxref("Promise")}} fue rechazada.

### Return value

Un objeto {{jsxref("Promise")}} que es rechazado por la razón específicada.

## Descripción

La función estática `Promise.reject` retorna un objecto {{jsxref("Promise")}} que es rechazado. Para fines de depuración y captura selectiva de error, se suele pasar por el parámetro `reason` un `instanceof` {{jsxref("Error")}}.

## Ejemplos

### Usando el método estático Promise.reject()

```js
Promise.reject(new Error('fail')).then(function() {
  // no entra en esta función
}, function(error) {
  console.log(error); // Stacktrace
});
```

## Especificaciones

| Specification                                                                        | Status                       | Comment                                 |
| ------------------------------------------------------------------------------------ | ---------------------------- | --------------------------------------- |
| {{SpecName('ES2015', '#sec-promise.reject', 'Promise.reject')}} | {{Spec2('ES2015')}}     | Initial definition in an ECMA standard. |
| {{SpecName('ESDraft', '#sec-promise.reject', 'Promise.reject')}} | {{Spec2('ESDraft')}} |                                         |

## Browser compatibility

{{Compat("javascript.builtins.Promise.reject")}}

## Ver también

- {{jsxref("Promise")}}
- [Selective error catching using the BlueBird Promise library](https://github.com/petkaantonov/bluebird#error-handling)
