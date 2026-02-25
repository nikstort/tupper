# Simulador Fórmula de Tupper

Simulador interactivo de la [fórmula autorreferencial de Tupper](https://en.wikipedia.org/wiki/Tupper%27s_self-referential_formula). Permite dibujar en un lienzo de píxeles blanco/negro, cambiar dimensiones, voltear ejes y obtener la constante **k** que codifica tu dibujo.

## Cómo usar

1. Abre `index.html` en un navegador.
2. **Dimensiones**: Cambia ancho y alto (p. ej. 106×17 clásico) y pulsa "Aplicar tamaño".
3. **Dibujar**: Clic izquierdo pinta (negro), clic derecho borra (blanco). Arrastra para dibujar/borrar en continuo.
4. **Voltear X / Y**: Refleja el lienzo horizontal o verticalmente (afecta también al valor de k).
5. **Zoom**: Deslizador para cambiar el tamaño de cada píxel en pantalla.
6. **Limpiar / Invertir**: Vacía el lienzo o invierte negro↔blanco.
7. **Calcular k**: Obtiene el número k; puedes copiarlo para usarlo en la fórmula en la región indicada.
8. **Guardados**: Escribe un nombre y pulsa "Guardar" para guardar la k actual. Las entradas se conservan en el navegador (localStorage) al recargar. Desde la lista puedes **Cargar** una k en el lienzo o **eliminarla** (✕).

## Fórmula

La desigualdad que se grafica (con tu alto **H** y ancho **W**) es:

```
1/2 < floor(mod(floor(y/H) · 2^(-H·floor(x) − mod(floor(y), H)), 2))
```

Región del plano: **0 ≤ x < W**, **k ≤ y < k + H**.

Con el **k** que genera el simulador, al representar esta desigualdad en esa región obtienes exactamente el dibujo del lienzo.
