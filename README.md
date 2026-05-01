# Trivial Pursuit Deluxe · Álgebra Lineal

Proyecto listo para publicar en GitHub Pages.

## Archivos del proyecto

- `index.html`: juego completo en un solo archivo.
- `.nojekyll`: evita que GitHub Pages procese el sitio con Jekyll.
- `README.md`: instrucciones básicas.

## Correcciones incluidas en esta versión

- Las respuestas de opción múltiple se mezclan aleatoriamente cada vez que aparece una pregunta.
- Las preguntas de opción múltiple usan 6 opciones posibles cuando corresponde.
- Se incluyen preguntas de opción múltiple, verdadero/falso, respuesta numérica entera y afirmaciones I, II y III.
- Cada pregunta tiene botón para detener/reanudar el tiempo de pregunta.
- Si un jugador responde correctamente, conserva el turno, pero solo hasta un máximo de 3 preguntas correctas consecutivas; después pasa obligatoriamente al siguiente jugador.
- El informe final se genera y descarga automáticamente como PDF al finalizar o anular la partida, sin abrir una vista previa automática del PDF.
- El PDF incluye resumen profesional, gráficas de notas, aciertos, incorrectas, desempeño por tema, registro de seguridad y plan de mejora individual.
- Si el estudiante regresa al menú final, aparece la opción de volver a la pantalla donde el docente ingresa la clave.
- Se agregó bloqueo grande de seguridad ante minimización, cambio de pestaña, pérdida de foco, salida de pantalla completa o intento detectable de pantallazo/impresión.
- Al tercer intento registrado, el quiz queda anulado y se descarga automáticamente el informe con el estado `QUIZ ANULADO`.
- Se retiró el botón de minimizar. La aplicación intenta mantenerse en pantalla completa desde la clave docente y durante todo el flujo.
- El botón `Cerrar Quiz y pestaña` finaliza el quiz, descarga el informe y luego intenta cerrar la pestaña del navegador.
- El juego muestra la hora actual en todo momento y ajusta el tablero a la resolución del dispositivo.

## Nota técnica importante

Los navegadores no pueden impedir al 100% las capturas hechas por herramientas externas del sistema operativo. Además, algunos navegadores pueden bloquear el cierre automático de una pestaña que no fue abierta por JavaScript; en ese caso se muestra una pantalla de quiz cerrado para que se cierre manualmente. El proyecto bloquea y registra los eventos que el navegador sí puede detectar: cambio de pestaña, minimización, pérdida de foco, salida de pantalla completa, PrintScreen cuando el navegador lo reporta, atajos de impresión/guardado y apertura de herramientas de desarrollo.

## Cómo subirlo a GitHub Pages

1. Crea un repositorio nuevo en GitHub.
2. Sube estos archivos directamente a la raíz del repositorio, no dentro de una carpeta.
3. En GitHub, entra a **Settings**.
4. Ve a **Pages**.
5. En **Build and deployment**, selecciona:
   - **Source:** Deploy from a branch
   - **Branch:** main
   - **Folder:** /root
6. Guarda los cambios.
7. GitHub mostrará el enlace público del juego después de unos minutos.

## Recomendación

Para evaluaciones, abre el juego en un navegador actualizado de escritorio, Chrome o Edge preferiblemente. La clave docente y la clave de desbloqueo son siempre la hora militar actual del dispositivo en formato `HHMM`, por ejemplo `0735` o `1842`.
