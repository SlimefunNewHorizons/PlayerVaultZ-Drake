# Como compilar PlayerVaultZ-Drake

Este repo es un **parche** sobre el plugin PlayerVaultZ 1.1.0 (de terceros, sin licencia publica). El jar original NO se versiona
y el `pom.xml` lo lee de `vendor/PlayerVaultZ-1.1.0.jar` (dependencia `system`). Por eso el CI de GitHub no puede compilarlo
(`.github/ci-skip`).

## Pasos
1. Consigue el **jar original** `PlayerVaultZ-1.1.0.jar` y verifica su hash:
   `SHA-256: F7225476AF8551898FA468112465C56C941E15185377B9690D642D7E28000CFB`
2. Colocalo en `vendor/` (esta ignorado por git).
3. `mvn clean package` (JDK 21). El resultado es `target/PlayerVaultZ-1.1.0-Drake.jar`.

## Ojo
- El `PlayerVaultZ.jar` que corre en Dallas **ya es el parcheado**: NO sirve como `vendor/` (otro hash). Tampoco los respaldos
  `legacy-plugins-2026-10-13/*` de Drive (son versiones parcheadas anteriores).
- Si perdiste el original: pidelo al autor del plugin o reconstruyelo desde su fuente original; sin el no se puede reproducir el parche.
- En Star: `~/ai-hub/scripts/build_seguro.sh 21 ~/workspace/drakescraft/PlayerVaultZ-Drake mvn -B clean package`.
