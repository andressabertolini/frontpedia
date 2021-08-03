## Editando o tema localmente e fazendo o push das alteraçõ

Ignore rules: Pra não sobrescrever o esquema de cores

config > setting_data.json

Vá para config.yml

ignore_files:

- config/settings_data.json

Na pasta do tema, rode:

```
theme watch
```

Erro: If you wish to make changes to it, then you will have to pass the --allow-live flag

```
theme watch --allow-live
```