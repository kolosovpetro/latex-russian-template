# LaTeX шаблон на русском

LaTeX шаблон на русском, который включает в себя базовую настройку CI/CD и шаблоны программ на языке Wolfram.

## Последовательность действий для сборки документа

- Установить `MikTeX`: https://miktex.org/download
- Обновить `MikTeX`
- Установить `SumatraPDF`: https://www.sumatrapdfreader.org/download-free-pdf-viewer
- Установить `Intellij IDEA Ultimate` среду разработки: https://www.jetbrains.com/idea/download/#section=windows
- Активировать `Intellij IDEA Ultimate`, надеюсь у вас есть ключ
- Установить плагин `TeXiFy IDEA` для `Intellij IDEA Ultimate`: https://plugins.jetbrains.com/plugin/9473-texify-idea
- Склонируйте данный репозиторий или используйте как шаблон на
  GitHub: `https://github.com/kolosovpetro/latex-russian-template.git`
- Откройте склонированный проект в среде разработки `Intellij IDEA Ultimate` и сконфигурируйте сборку документа
    - LaTeX Configuration
      ![LaTeX Configuration](img/latex_configuration.PNG?raw=true "LaTeX Configuration")
    - BibTeX Configuration
      ![BibTeX Configuration](img/bibtex_configuration.PNG?raw=true "BibTeX Configuration")
- Сконфигурируйте обратный поиск `Intellij IDEA` для `SumatraPDF`: `Tools -> LaTeX -> Configure Inverse Search`
- Запустите сборку документа сочитанием клавиш `Shift + F10`

## Конфигурация CI / CD

Для корректной работы CI / CD установите `GH_ACCESS_TOKEN` в секреты Github:

- `GH_ACCESS_TOKEN`: Generate GitHub Personal access token at
  `Settings -> Developer Settings -> Personal access tokens -> Generate mew token`

## Политика срабатывания CI / CD

- `build-pdf.yml` срабатывает при `pull_request`, `push` в ветку `develop`
- `build-and-deploy-pdf.yml` публиует собранный PDF документ на удаленный репозиторий `GitHub Pages`.
  Срабатывает на событии `push` в ветку `master`

## Пример шаблона

Скомпирированный шаблон выглядит следующим образом

<p align="center">
  <img src="img/template_example.PNG" alt="template_example"/>
  <img src="img/template_example2.PNG" alt="template_example"/>
  <img src="img/template_example3.PNG" alt="template_example"/>
</p>

## Лицензия

This work is licensed
under [Attribution-NonCommercial-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode)
license
