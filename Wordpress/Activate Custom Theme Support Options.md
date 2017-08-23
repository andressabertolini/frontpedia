## Activate Custom Theme Support Options

```
register_setting('sunset_theme_support','post_formats','sunset_post_formats_callback');
add_settings_field('post-formats','Post Formats','sunset_post_formats','alecaddd_sunset_theme','sunset-theme-options');

function sunset_post_formats_callback($input){
	return $input;
}

function sunset_theme_options(){
    echo 'Activate and Deactivate specific Theme Support Options';
}

function sunset_post_formats(){
    $options = get_option('post_formats');
    $formats = array('aside','gallery','link','image','quote','status','video', 'audio', 'chat');
    $output = '';
    foreach($formats as $format){
	    $checked = ( @$options[$format] == 1 ? 'checked' : '' );
			//this @ is to do if the array exists
	    $output .= '<label><input type="checkbox" id="'.$format.'" name="post_formats['.$format.']" value="1" '.$checked.' />'.$format.'</label><br>';
    }
    echo $output;
}
```