Create a theme-admin.js file in the js folder

Inside the enqueue.php file

```
wp_register_script('sunset-admin-script', get_template_directory_uri().'/js/sunset.admin.js', array('jquery'), '1.0.0',true);
//o array('jquery') indica que precisamos de jquery pra esse arquivo funcionar
//o true no final indica que queremos incluir no footer
wp_enqueue_media(); //chama os scripts pra usar o media uploader
wp_enqueue_script('sunset-admin-script');
//esse id (primeiro parametro) usamos aqui pra chamar 
```

## Media Uploader

Inside function-admin.php
```
register_setting('sunset-settings-group','profile_picture');
add_settings_field('sidebar-profile-picture', 'Profile Picture', 'sunset_sidebar_profile_picture', 'alecaddd_sunset','sunset-sidebar-options');

function sunset_sidebar_profile_picture(){
    $profilePicture = esc_attr(get_option('profile_picture'));
    echo '<input type="button" class="button button-secondary" value="Upload Profile Picture" id="upload-button"/><input type="hidden" name="profile_picture" value="'.$profilePicture.'" id="profile-picture"/>';
}
```