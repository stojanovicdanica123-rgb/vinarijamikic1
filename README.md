# Vinarija Mikić — sajt (ravna struktura)

Svi fajlovi su u jednom nivou, bez foldera — namerno, jer GitHub-ov upload preko browsera
ne čuva foldere kad se fajlovi dodaju jedan po jedan.

## Kako okačiti

1. U repozitorijumu: **Add file → Upload files**, pa označi **sve** fajlove iz ovog foldera i prevuci ih.
2. Commit changes.
3. Settings → Pages → Deploy from a branch, `main`, `/ (root)` → Save.
4. Sajt je na `https://<korisnik>.github.io/<repo>/` (kod tebe: stojanovicdanica123-rgb.github.io/vinarijamikic/).

Ako u repozitorijumu već postoje stari fajlovi `index (1).html` i `index (2).html` — obriši ih,
zbunjuju samo. `.nojekyll` je skriven; ako se ne pojavi pri prevlačenju, napravi ga preko
Add file → Create new file → ime `.nojekyll`.

## Fajlovi

    index.html              cela strana
    o-nama.html             preusmerenje na „O nama"
    nasa-vina.html          preusmerenje na katalog vina
    support.js              runtime
    *.woff2                 Marcellus i Alegreya Sans (lokalno, bez Google Fonts)
    foto-*.jpg              fotografije vina
    *.png                   flaše sa providnom pozadinom, logo
    hero-vinograd.jpg, pivnice-rajac.jpg, podrum.jpg
    klip-3.mp4              video u traci „Dođite u podrum"

## Pre produkcije

- Dva 4K klipa su izostavljena zbog GitHub limita od 25 MB po fajlu; prekodiraj ih
  (`ffmpeg -i klip-1.mp4 -vf scale=1920:-2 -c:v libx264 -crf 25 -preset slow -an -movflags +faststart klip-1.mp4`)
  i dodaj u traku.
- Etikete nose nazive `HelgVoria` / `Melin` i mesto `Indija` — zameniti pravim Mikić etiketama.
- Logo je 270×270; za retinu treba vektor i krem verzija za tamne sekcije.
- Meni „Aktuelno" vodi na sekciju Nagrade; treba mu sadržaj.
