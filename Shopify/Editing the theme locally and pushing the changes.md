## Editing the theme locally and pushing the changes

Ignore rules: To avoid overwriting the color scheme

config > setting_data.json

Go to config.yml

ignore_files:

- config/settings_data.json

In the theme folder, run:

```
theme watch
```

Erro: If you wish to make changes to it, then you will have to pass the --allow-live flag

```
theme watch --allow-live
```