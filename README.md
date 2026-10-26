# rea

## META
- id: rea
- owner: EduBalderas
- visibility: public
- idioma: mixto
- estado: estable
- tipo: fork
- nivel: L4
  - L0=gobernanza/política
  - L1=marca/metodología
  - L2=flujo/arquitectura
  - L3=producto ejecutable
  - L4=herramienta
- familia: desconocido
- origen: upstream:https://github.com/morluto/rea
- experimento: no
- nacido_de: morluto/rea
- orquestado_por: N/A
- brief_desde: N/A

## OBJETIVO
Herramienta local de ingeniería inversa, con CLI y servidor MCP compartidos, para inspeccionar binarios, aplicaciones y comportamiento en tiempo de ejecución y devolver evidencia con sus limitaciones.

## QUE_CONTIENE
- Paquete npm `rea-agents` 6.4.0 (`package.json`): binarios `rea` y `rea-agents`, licencia MIT y motores Node.js `^22.19.0 || ^24.11.0 || >=26.0.0`.
- Servidor MCP `io.github.morluto/rea` (`server.json`): transporte stdio, arranque con `npx` y argumento `mcp`.
- Código TypeScript en `src/`: CLI, contratos, dominio y adaptadores (Hopper, Ghidra, IDA, JEB, Android/JADX, Frida, .NET, JavaScript, navegador, firmware, WASM, EVM, SQLite, pcap y señales, entre otros).
- Puentes en `bridge/` para Hopper, Ghidra, Android, mitmproxy, pwntools, pwndbg, proceso y componentes nativos.
- Documentación de flujos en `docs/`, sitio en `website/`, y guías de contribución en `AGENTS.md` y `CONTRIBUTING.md`.
- Pruebas en `tests/`, artefacto nativo de Windows en `native/`, terceros en `third_party/` y avisos en `THIRD_PARTY_NOTICES.md`.
- README canónico en inglés y traducciones (`README_es.md`, `README_zh.md` y el resto de `README_*.md`).
- `DISCLAIMER.md`, `SECURITY.md`, `LICENSE` y el directorio `experiments/`.

## CARACTERISTICAS
- El mismo flujo de análisis se usa desde el CLI y desde el servidor MCP (`package.json`, `server.json`, `AGENTS.md`).
- El análisis corre en local; cada resultado incluye la evidencia y las limitaciones de la conclusión.
- La inspección estática de JavaScript/Electron y de ensamblados .NET no necesita un motor nativo. El análisis nativo usa una instalación existente de Hopper, Ghidra o IDA.
- `rea setup` muestra los cambios previstos y exige aprobación antes de escribir configuración o instalar Hopper. Ghidra e IDA son bring-your-own.
- IDA es de solo lectura: no guarda ni cierra una base de datos GUI adjunta. Ghidra usa bases efímeras y no modifica los bytes del ejecutable. Windows Ghidra P0 no tiene autoridad de mutación.
- La documentación de análisis cubre binarios nativos, diseño ELF, binarios Go, WASM, bytecode EVM, SQLite, JavaScript/Electron, sitios, capturas de red, .NET, APK, dispositivos Android, proyectos JEB, Flutter, firmware, paquetes y comportamiento de procesos.
- Requiere Node.js 22.x (>=22.19), 24.x (>=24.11) o 26+, además de npm.

## FUERA_DE_ALCANCE
- Flujos hechos para derrotar empaquetado comercial o virtualización de código y recuperar automáticamente el código protegido (`CONTRIBUTING.md`).
- Evasión anti-depuración o anti-instrumentación, y bypass de DRM, licencias, anti-cheat o controles de acceso.
- Automatización de exploits o payloads, robo de credenciales, persistencia encubierta, acceso no autorizado o ataques masivos.
- El instalador no instala ni actualiza Homebrew, Node.js, npm, Java ni Ghidra (`AGENTS.md`).
- REA no concede licencia, clave ni activación de IDA Pro, Hopper o JEB.
- Usos descritos como no admitidos en `DISCLAIMER.md`: eludir DRM, cheats, saltar autenticación en sistemas no autorizados, copiar software propietario o evadir políticas de proveedores de modelos.

## RELACIONES
- Fork público de https://github.com/morluto/rea (parent `morluto/rea`). Este repo: https://github.com/EduBalderas/rea.
- Paquete npm: https://www.npmjs.com/package/rea-agents (`rea-agents` 6.4.0).
- Sitio del repo: https://rea.tools. El campo `homepage` de `package.json` apunta a https://github.com/morluto/rea#readme.
- Issues declarados por el paquete: https://github.com/morluto/rea/issues.
- Identidad MCP: `io.github.morluto/rea` (`mcpName` en `package.json` y `name` en `server.json`).
- Skill publicada: https://skills.sh/morluto/rea/reverse-engineer-anything.
- Comunidad upstream: https://discord.gg/GkcryMnJDM.

## ETIQUETAS
- reverse-engineering
- binary-analysis
- agents
- agent-skills
- cli
- mcp-server
- model-context-protocol
- static-analysis
- disassembler
- decompiler
- mcp
- hopper
- typescript
- mit
- fork

## TOPICS_GITHUB
- N/A
