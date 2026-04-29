# aittimes-cdn

Публичный CDN для автопостинга @aittimes IG.

## Назначение
Хостинг medi-файлов (PNG/MP4) для Meta Graph API publishing — Drive 303-redirects ломают reel video upload, поэтому видео идёт через github raw.

## Strict whitelist (.gitignore)
В этот репо могут попасть ТОЛЬКО:
- `*.png`, `*.jpg`, `*.jpeg`, `*.mp4`, `*.webp`
- `.gitignore`, `README.md`

Всё остальное запрещено по умолчанию (см. `.gitignore`). Никаких скриптов, токенов, секретов, конфигов.

## Retention
Файлы старше 30 дней удаляются скриптом `aittimes_cdn_cleanup.py` в основном workspace.

## URL формат
`https://raw.githubusercontent.com/ttimesai-star/aittimes-cdn/main/<filename>`
