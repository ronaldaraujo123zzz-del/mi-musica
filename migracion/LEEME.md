# Llave vieja (quemada)

`llave-vieja-QUEMADA.jks` es la llave con la que se firmó NEAR Music hasta la
versión 15. Su contraseña es `mimusica123`.

**No es un secreto y no debe tratarse como tal.** Estuvo publicada en este
repositorio dentro de `android.zip`, y sigue en el historial de git, donde no se
puede borrar. Por eso se dejó de usar.

## Para qué sigue aquí

Solo para una cosa: generar el certificado de autorización (*signing lineage*)
que permite que los teléfonos acepten la versión nueva como actualización de la
vieja, sin desinstalar.

El APK se firma con la llave nueva (`near-music.jks.enc`, cifrada, en la raíz
del repositorio). Este archivo únicamente aporta la prueba de que la llave vieja
autoriza a la nueva a sustituirla.

## Qué NO hace

No sirve para firmar versiones nuevas. Una vez que un teléfono tiene una versión
rotada instalada, Android rechaza cualquier APK firmado solo con esta llave.

## Cuándo se puede borrar

Cuando todos los teléfonos tengan ya una versión rotada (de la 18 en adelante).
A partir de ahí el certificado de autorización deja de hacer falta y se puede
quitar tanto este archivo como el paso que lo usa en el workflow.
