## Editing the theme locally and pushing the changes

Ignore rules: Pra não sobrescrever o esquema de cores

config > setting_data.json

Go to config.yml

ignore_files:

- config/settings_data.json

Na pasta do tema, run:

```
theme watch
```

Erro: If you wish to make changes to it, then you will have to pass the --allow-live flag

```
theme watch --allow-live
```