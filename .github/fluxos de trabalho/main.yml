Nome : Gerar Dados

em :
  cronograma : # executar a cada 12 horas
    - cron : " * */12 * * * "
  workflow_dispatch :

trabalhos :
  construir :
    nome : Jobs para atualizar dados
    run-on : ubuntu-latest
    passos :
      # Animação de Cobra
      - usa : Platane/snk@master
        id : cobra-gif
        com :
          github_user_name : rafaballerini
          svg_out_path : dist/github-contribution-grid-snake.svg

      - usa : crazy-max/ghaction-github-pages@v2.1.3
        com :
          target_branch : saída
          build_dir : dist
        ambiente :
          GITHUB_TOKEN : ${{ segredos.GITHUB_TOKEN }}
