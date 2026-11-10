<div align="center">

[Português](README.md) · [English](README.en.md) · **Español**

# Poker MTT BI

**La app donde sigo mis torneos de póker: paneles, las finanzas del equipo y un asistente con IA local que responde y registra cosas por mí.**

<img src="docs/img/resumo-escuro.png" alt="Pantalla Resumen, tema oscuro" width="900">

<sub>Código cerrado · imágenes con datos ficticios · la interfaz de la app está en portugués</sub>

</div>

## Por qué existe

Juego torneos online (MTT) todos los días, en varias cuentas, dentro de un equipo. El equipo tiene reglas propias de reparto: makeup, deal, rakeback y meta semanal. Antes lo llevaba todo en una hoja de cálculo, y revisar que cada pago coincidiera me llevaba horas.

Hoy marco los registros del día y la app hace el resto. Muestra cómo voy, calcula lo que el equipo me debe y me avisa cuando algo no cuadra.

## Resumen

El mes de un vistazo: ganancia, ROI, la curva de la carrera, el mejor torneo, el resultado por categoría y por cuenta, y cuánto falta para la meta de rake de la semana.

<img src="docs/img/resumo-claro.png" alt="Pantalla Resumen, tema claro" width="900">

## Diario y Torneos

El calendario muestra cada día jugado y su resultado. Al hacer clic en un día aparecen sus destacados. En Torneos está la lista completa, con búsqueda, filtros y exportación a hoja de cálculo.

<img src="docs/img/diario.png" alt="Pantalla Diario" width="900">

<img src="docs/img/torneios.png" alt="Pantalla Torneos" width="900">

## Finanzas

La app rehace el makeup día a día desde el primer torneo, con las reglas del equipo de cada época. Muestra la semana actual, las semanas cerradas, los retiros recibidos y cuánto falta para liberar el rakeback.

<img src="docs/img/financeiro.png" alt="Pantalla Finanzas" width="900">

## Pool

Pego el informe diario que manda el equipo. La app revisa los totales, reparte la cuota de cada jugador y suma el mes.

<img src="docs/img/pool.png" alt="Pantalla Pool" width="900">

## Asistente con IA local

Un chat dentro de la app, con un modelo de lenguaje (Qwen, `qwen3.5:4b`) que corre en mi propia tarjeta gráfica. No tiene costo de API, y ningún dato sale de la computadora.

- **Pregunto en vez de buscar:** "¿cuánto gané en noviembre?", "¿qué cuenta perdió más en octubre?", "¿cuánto me pagó el equipo en septiembre?".
- **Registra por mí:** escribo "cayeron 136,20 del cierre diario del 05/11 en el banco" y arma el retiro. No se guarda nada hasta que hago clic en **Gravar** (Guardar).
- **Me avisa:** un pago calculado que no llegó, un día de la pool sin informe, un registro que necesita revisión.

El modelo solo entiende el pedido. Las cuentas las hace la propia app, así que el asistente muestra los mismos números que las demás pantallas.

<img src="docs/img/assistente.png" alt="Asistente respondiendo una pregunta y proponiendo un retiro" width="900">

## Grilla

La grilla semanal de torneos del equipo, tomada de su hoja de cálculo.

<img src="docs/img/grade.png" alt="Pantalla Grilla" width="900">

## Hecho con

Lo construí orquestando agentes de IA (Claude Code y Gemini), al estilo *vibe coding*: defino lo que hace la app y sus reglas, los agentes escriben el código, y yo lo reviso y pruebo en el uso diario.

Por debajo: C# y .NET 10 en el servidor, React y TypeScript en la interfaz, SQLite como base de datos y Ollama para el modelo local. Corre entero en mi computadora, con tema claro y oscuro.

---

<sub>Hecho por **Yan Camargo** · [LinkedIn](https://www.linkedin.com/in/yan-ca%C3%AA-camargo-38b1002a1/) · © 2026, todos los derechos reservados ([LICENSE](LICENSE))</sub>
