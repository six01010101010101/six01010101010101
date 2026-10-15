<!-- ═══════════════════════════ BOOT / BANNER ═══════════════════════════ -->
<div align="center">

<img src="[capsule-render.vercel.app](https://capsule-render.vercel.app/api?type=waving&color=0:000000,50:0f0c29,100:00f5ff&height=220&section=header&text=KEN%20KOBAYASHI&fontSize=62&fontColor=00f5ff&fontAlignY=38&desc=//%20SYSTEM%20ONLINE%20::%20FULL%20STACK%20%26%20UX/UI%20DEVELOPER&descSize=16&descAlignY=60&descAlign=50&animation=fadeIn)" width="100%"/>

<img src="[readme-typing-svg.demolab.com](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=15&duration=1800&pause=400&color=39FF14&center=true&vCenter=true&multiline=true&repeat=false&width=620&height=110&lines=%3E+Initializing+K.E.N+Neural+Interface...;%3E+Loading+modules+%5B%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%5D+100%25;%3E+Access+granted.+Welcome%2C+visitor)" alt="boot"/>

<br/>

<img src="[readme-typing-svg.demolab.com](https://readme-typing-svg.demolab.com?font=Orbitron&weight=600&size=24&duration=3000&pause=800&color=00F5FF&center=true&vCenter=true&width=700&lines=Full+Stack+Developer+%E2%9A%A1;UX+%26+UI+Designer+%F0%9F%8E%A8;Estudante+%40+FIAP+Paulista+%F0%9F%9A%80;Construindo+o+futuro%2C+um+commit+por+vez)" alt="Typing SVG"/>

<br/><br/>

<a href="[github.com](https://github.com/SEU_USUARIO)"><img src="[img.shields.io](https://img.shields.io/github/followers/SEU_USUARIO?label=FOLLOWERS&style=for-the-badge&color=00f5ff&labelColor=0d1117&logo=github)"/></a>
<img src="[komarev.com](https://komarev.com/ghpvc/?username=SEU_USUARIO&label=PROFILE%20VIEWS&color=00f5ff&style=for-the-badge&labelColor=0d1117)"/>
<img src="[img.shields.io](https://img.shields.io/badge/STATUS-ONLINE-39FF14?style=for-the-badge&labelColor=0d1117)"/>

</div>

<img src="[user-images.githubusercontent.com](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)" width="100%"/>

<!-- ═══════════════════════════ SOBRE MIM ═══════════════════════════ -->
## <img src="[media.giphy.com](https://media.giphy.com/media/W5eoZHPpUx9sapR0eu/giphy.gif)" width="28"/> `> SOBRE_MIM.exe`

<table>
<tr>
<td width="60%" valign="top">

```yaml
user:       Ken Kobayashi
age:        21
location:   São Paulo, Brasil 🇧🇷
education:  FIAP Paulista
role:       Full Stack Developer | UX & UI Designer
mission:    Criar interfaces bonitas, rápidas e humanas
status:     Sempre aprendendo 🧠
ken@kobayashi:~$ ./missions --status

[✔] Dominar HTML5, CSS3 e JavaScript moderno
[▶] Aprofundando em React, Next.js e TypeScript ........ 70%
[▶] Construindo APIs com Node.js ....................... 55%
[▶] Design Systems e UX Research no Figma .............. 65%
[ ] Contribuir com projetos Open Source
[ ] Conquistar minha vaga como Dev Full Stack
[ ] Explorar integrações com Inteligência Artificial

ken@kobayashi:~$ █
name: Generate Snake

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches: [main]

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark&color_snake=#00f5ff&color_dots=#161b22,#0e4429,#006d32,#26a641,#39d353

      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
