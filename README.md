# AI platformas video (priekšskatījums)

Mitigate AI platformas produkta un apmācību video, lai apskatītu, kā tie izskatās, pirms lemjam par
pastāvīgu vietu. Lapa: https://janatrapane.github.io/ai-platform-videos/

Video tiek ierakstīti ar video komplektu AI platformas repo (`script/video/`, skils `product-video`).
Visi dati video ir izdomāti.

## Jauna video pievienošana

1. Web versija no 1080p galvenā faila:
   `ffmpeg -i <output>-<lv>.mp4 -vf scale=1600:900:flags=lanczos -c:v libx264 -preset slow -crf 22 -pix_fmt yuv420p -movflags +faststart videos/<id>-<versija>-<lv>.mp4`
2. Priekšskata attēls (`thumbnails.mjs` izvade) → `videos/<id>-<versija>-<lv>.jpg`.
3. Ieraksts `videos.json` (virsraksts, apraksts, garums, valodas).
4. Mainītam video jauna versija (`v2`), veco failu nepārraksta.
