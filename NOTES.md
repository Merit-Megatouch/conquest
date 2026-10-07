# CONQUEST (conquest)

Status: runs (legacy engine, smoke-tested 2026-10-07). Draws, touch zones work; plays from the title screen.

## Checklist
- [ ] Window size in game.conf matches the largest PNG (notes/scaffold.md)
- [ ] Every symbol in notes/unresolved.txt has a stand-in in src/host/loader_services.cpp
      (`make analyze GAME=conquest` until it reports 0)
- [ ] First run: `make run GAME=conquest DEBUG=shots` — crash trace + screenshots in notes/shots
- [ ] Paths: `make run GAME=conquest DEBUG=files`; engine trace: `mkdir -p data/var/merit/debug/files && touch data/var/merit/debug/files/resource_locator`
- [ ] Reference code: `make decompile GAME=conquest`
- [ ] Translations + help text appear (gamedata/translations/conquest.utf8)
- [ ] Sound and music play (`DEBUG=sound`)
- [ ] A full game plays through (`DEBUG=profile` to catch stalls and old-malloc bugs)

## Log
<!-- dated notes: what broke, what fixed it -->

- 2026-10-07 — runs on src/legacy with no stubs; Draws, touch zones work; plays from the title screen.
