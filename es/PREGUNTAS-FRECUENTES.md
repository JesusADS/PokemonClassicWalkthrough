# Preguntas frecuentes

## ¿Dónde está Cedar?

Cedar viaja por distintos puestos de control y Centros Pokémon a medida que consigues medallas. Si no sabes dónde se encuentra, habla con los demás ayudantes del laboratorio de Oak para recibir una pista.

Los objetos y requisitos conocidos están reunidos en el [índice de objetos de Cedar](INDICES-DE-CONSULTA.md#objetos-entregados-por-cedar).

## ¿Cómo evolucionan los Pokémon que antes exigían intercambio?

Kadabra, Machoke, Graveler y Haunter pueden evolucionar mediante Piedra Poder. Otros casos con objeto equipado conservan en el código el método de intercambio. Consulta [Evoluciones especiales](EVOLUCIONES-ESPECIALES.md) para ver la distinción completa.

## ¿Cómo consulto los IV y EV?

Abre el resumen del Pokémon y entra en la vista de estadísticas. La interfaz muestra un aviso para pulsar A y alternar entre las vistas de IV y EV.

El DexNav también representa la calidad de los IV mediante una valoración de 0 a 3 estrellas.

## ¿Por qué solo Pikachu puede seguirme?

Durante la historia principal se conserva el comportamiento de *Pokémon Amarillo*: Pikachu es el compañero disponible. Después de convertirte en Campeón se habilitan otros seguidores.

## ¿Cómo funcionan las MO fuera de combate?

Puedes usar una MO cuando posees el objeto correspondiente y la medalla necesaria. No es necesario enseñársela a un Pokémon en las condiciones documentadas por el hack.

Excavar puede usarse teniendo su MT. Teletransporte requiere llevar un Pokémon Psíquico compatible.

## ¿Por qué la Battle Tower funciona como una tienda?

El sistema original de combates de la Battle Tower no funciona correctamente en esta base del proyecto. En *Pokémon Classic* se reutiliza principalmente como tienda para gastar los Battle Points obtenidos en rematches y combates especiales.

## No puedo volar a Ciudad Fucsia o a la entrada del Túnel Roca

Visita primero a pie Ciudad Fucsia y la entrada del Túnel Roca en la Ruta 10. La documentación explica que estas visitas activan los destinos de Vuelo cuando sus indicadores no se han registrado todavía.

## ¿Dónde consigo las cañas?

| Objeto | Localización |
|---|---|
| Caña Vieja | Casa del Gurú Pescador de Ciudad Carmín |
| Caña Buena | Casa del Gurú Pescador de Ciudad Fucsia |
| Supercaña | Hermano menor del Gurú Pescador en Ruta 12 |

Los encuentros que requieren una caña aparecen marcados con `🎣` en cada volumen.

## ¿La documentación original describe todos los equipos de combate?

No. La documentación original omite algunos equipos y combates. Cuando existen datos internos en la copia local de Pokémon Classic v1.5 —como la segunda Liga, Oak, los rematches de gimnasio y los entrenadores con Mega Evolución— esta guía los incorpora desde `trainer_parties.h` y los scripts de cada mapa. Solo se marcan como pendientes los datos que tampoco aparecen en el código.

## ¿Puedo reutilizar una partida de una versión anterior?

La documentación contiene instrucciones para migraciones antiguas entre v1.3 y v1.4, pero esta guía está preparada para v1.5. Conviene consultar el [repositorio actual del juego](https://github.com/DaniRainbow/pokeclassic) antes de migrar una partida entre versiones.

[← Índice principal](README.md) · [Cómo usar la guía](COMO-USAR-LA-GUIA.md) · [Índices de consulta](INDICES-DE-CONSULTA.md)
