## Custom Options

Dentro da função de add_admin_page, ativar o custom settings:

```jsx
//Activate Custom Settings
add_action('admin_init','theme_custom_settings');
```

Criar a função declarada acima:

```jsx
function theme_custom_settings(){
		add_settings_section('sunset-sidebar-options', 'Sidebar Options','sunset_sidebar_options','alecaddd_sunset');
    
		register_setting('settings-group','first_name'); //essa função reserva um espaço no banco de dados para um conjunto de campos
    add_settings_field('sidebar-name', 'First Name', 'sunset_sidebar_name', 'alecaddd_sunset','sunset-sidebar-options');
}

function sunset_sidebar_options(){
    echo 'Customize your Sidebar Information';
}

function sunset_sidebar_name(){
    $firstName = esc_attr(get_option('first_name'));
    echo '<input type="text" name="first_name" value="'.$firstName.'" />';
}
```

Na página de template, criar um form do tipo post com o action vazio
```
<?php settings_errors() ?>
<form method="post" action="options.php">
		<?php settings_fields('sunset-settings-group');?>
    <?php do_settings_sections('alecaddd_sunset');?>
		<?php submit_button(); ?>
</form>
```