---
name: feedback-estilo-guiones
description: El usuario no quiere que se usen guiones largos (-- o ---) como recurso estilístico parentético en el texto
metadata:
  type: feedback
---

No usar guiones largos (em dash `---` o en dash `--` en LaTeX, o `—` en Unicode) como recurso parentético en el texto del documento. Tampoco abusar de los dos puntos (`:`): si se puede reemplazar por una coma, "donde", o reestructurando la oración, hacerlo.

**Excepción explícita:** esto NO aplica a palabras compuestas legítimas del español ni a nombres propios con guion (cliente-servidor, scikit-learn, YOLO11n-pose, publish/subscribe). El usuario aclaró puntualmente que esas se dejan como están; solo se evita el guion/raya usado como puntuación para meter una aclaración al vuelo.

También evitar el tono "meta" que describe la estructura del propio documento ("esta sección no repite...", "a diferencia de la sección siguiente, que describe X, esta sección describe Y..."). Ir directo al contenido en vez de anunciar qué va a hacer el texto.

**Why:** Al usuario le parece que se abusa de ese recurso estilístico y que ese tono metarreferencial (junto con el uso de dos puntos/guiones para aclaraciones) hace que el texto suene generado por IA, algo especialmente sensible en una tesis.

**How to apply:** No introducir guiones largos ni tono meta en texto nuevo que se redacte para los capítulos del informe. No tocar los guiones largos que ya existían en el documento original, ni las palabras compuestas con guion; solo aplica al texto nuevo que Claude escriba y a la puntuación usada como recurso de aclaración.
