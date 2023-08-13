### Olá eu sou o Tiago Teixeira 👋

- 🌱 Estou a estudar no momento Python
- 📫 Discord : tiago.__.teixeira
- ⚡ Factos sobre mim : Gosto de me divertir e de aprender coisas novas

 <img align='right' height="170em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=tiagoteixeira9&layout=compact&langs_count=7&theme=dracula"/>
</div>
</div>


name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
