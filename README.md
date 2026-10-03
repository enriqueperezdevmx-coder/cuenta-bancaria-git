# Cuenta bancaria — Git y pull requests

**Autor:** Enrique Pérez Sánchez

## Cómo correr
./correr.sh

## Mis pull requests
| # | Qué cambió |
|---|---|
| 1 | El estado de cuenta muestra cuántos retiros se hicieron y cuántos fueron gratis |
| 2 | README y evidencia de la práctica |

## Boleto de salida

1. **¿Qué diferencia hay entre `git add` y `git commit`?**  
   **Respuesta:** `git add` traslada los cambios de tu carpeta de trabajo al área de preparación (*staging*), seleccionando exactamente qué archivos o modificaciones formarán parte del siguiente guardado. `git commit` toma todo lo que está acumulado en el área de preparación y lo guarda de forma definitiva en el historial del repositorio con un identificador único y un mensaje explicativo.

2. **¿Por qué después del merge en GitHub tu main de Ubuntu no tenía el cambio hasta que hiciste `git pull`?**  
   **Respuesta:** Porque la operación de merge ocurrió en los servidores de GitHub (la nube remota). Git es un sistema distribuido y las ramas locales no se actualizan de forma automática ni consultan a internet por sí solas. La máquina local no recibe los nuevos commits hasta que se invoca `git pull`, que solicita a `origin` las actualizaciones y avanza el puntero de `main`.

3. **Abriste un PR y después hiciste otro commit en la misma rama. ¿Qué pasó con el PR?**  
   **Respuesta:** El nuevo commit se agregó de manera automática al mismo pull request. Un PR no es una foto fija de un momento, sino un seguimiento dinámico a la rama origen (*compare*); por lo tanto, cualquier commit que se suba mediante `git push` a esa rama se incorpora de inmediato a la conversación del PR sin necesidad de abrir uno nuevo.

4. **¿Por qué en un equipo nadie hace cambios directamente en `main`?**  
   **Respuesta:** Para garantizar la estabilidad del proyecto y evitar que código roto o incompleto afecte a los demás desarrolladores o al entorno de producción. Trabajar en ramas secundarias permite que los cambios sean revisados por compañeros (*code review*), probados de forma aislada y documentados con claridad antes de su integración definitiva mediante un pull request.