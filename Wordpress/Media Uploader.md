Create a theme-admin.js file in the js folder

Inside the enqueue.php file

```
wp_register_script('sunset-admin-script', get_template_directory_uri().'/js/sunset.admin.js', array('jquery'), '1.0.0',true);
//the array('jquery') indicates that we need jquery for this file to work
//true at the end indicates that we want to include it in the footer
wp_enqueue_media(); //call the scripts to use the media uploader
wp_enqueue_script('sunset-admin-script');
//this id (first parameter) we use here to call
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