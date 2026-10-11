# Alquimia Culinaria

PWA gamificada de cocina. Monorepo Nx con pnpm. Windows + PowerShell.

## Estructura
- apps/web: Angular (standalone, signals, @angular/pwa)
- apps/api: NestJS (monolito modular, arquitectura hexagonal ligera)
- libs/contracts: esquemas Zod compartidos (fuente única de tipos)
- supabase/migrations: SQL versionado

## Comandos
- pnpm nx serve web   (arranca web en :4200 y api en :3000/api)
- pnpm nx serve api   (solo la api)
- pnpm nx test <proyecto> | pnpm nx lint <proyecto>

## Reglas
- Todo JSON de la IA se define en libs/contracts y se valida con Zod.
- El modelo de IA se lee de la variable OPENAI_MODEL; nunca en el código.
- No leas ni escribas ficheros .env; usa .env.example.
- Migraciones SQL nuevas en supabase/migrations, nunca editar las antiguas.
- Antes de dar una tarea por terminada: tests y lint en verde.
- Textos de la interfaz en español de España.
- Commits en formato convencional (feat:, fix:, chore:...).

## Plan y seguimiento
- Plan completo del MVP: docs/PLAN.md
- Estado y siguiente paso: docs/PROGRESO.md
- Al empezar una sesión, lee PROGRESO.md. Al terminar una tarea, márcala y añade la siguiente.