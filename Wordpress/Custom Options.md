## Custom Options

Inside the add_admin_page function, activate the custom settings:

```
//Activate Custom Settings
add_action('admin_init','theme_custom_settings');
```

Create the function declared above:

```
function theme_custom_settings(){
		add_settings_section('sunset-sidebar-options', 'Sidebar Options','sunset_sidebar_options','alecaddd_sunset');
    
		register_setting('settings-group','first_name'); //This function reserves a space in the database for a set of fields
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

On the template page, create a post-type form with an empty action
```
<?php settings_errors() ?>
<form method="post" action="options.php">
		<?php settings_fields('sunset-settings-group');?>
    <?php do_settings_sections('alecaddd_sunset');?>
		<?php submit_button(); ?>
</form>
```