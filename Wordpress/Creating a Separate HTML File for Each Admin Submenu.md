Create the file admin/pages-templates/general-admin.php. This file will contain the HTML for the page.

```
<h1>General Admin</h1>
<p>Customize</p>
```

In the file function.admin.php:

```
function theme_page_general() {
    require_once(get_template_directory() . '/admin/pages-templates/general-admin.php');
}
```