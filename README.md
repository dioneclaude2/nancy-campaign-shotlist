# nancy-campaign-shotlist — recovered source

Recovered 26 Aug 2026 from the live Vercel deployment
(project `prj_QFkn1JlftUcDAKsNhDAHfJDh6GmL`, deployment `dpl_XQLqePKdJ18WNbrW668xTNcqxNpm`).

## What's here

- `index.html` — the exact source. One self-contained file: inline `<style>`,
  inline `<script>`, relative `assets/` paths. This is the real backup.
- `nancy-shotlist-standalone.html` — same file, asset paths rewritten to absolute
  URLs on the live deployment. Opens and works anywhere, no assets folder needed.
- `ASSETS.txt` — the 45 image/video/svg files the site loads.

Only external dependency is Google Fonts (Poppins, DM Sans, JetBrains Mono).

## To rebuild the full project on your computer

    mkdir nancy-campaign-shotlist && cd nancy-campaign-shotlist
    cp /path/to/index.html .
    wget -x -nH -i <(sed 's|^|https://nancy-campaign-shotlist.vercel.app/|' ASSETS.txt)

Then push it to a private GitHub repo and link the repo in Vercel, so the next
deploy comes from Git instead of a folder upload.

## To redeploy

    vercel --prod
