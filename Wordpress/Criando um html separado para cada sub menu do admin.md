## Criando um html separado para cada sub menu do admin

Criar o arquivo **admin/pages-templates/general-admin.php**, esse arquivo vai ter o html da página

```jsx
<h1>General admin</h1>
<p>Customize</p>
```

Na página function.admin.php:
```
function theme_page_general(){
    require_once(get_template_directory().'/admin/pages-templates/general-admin.php');
}
```