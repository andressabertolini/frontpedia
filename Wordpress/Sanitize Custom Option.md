```
register_setting('sunset-settings-group','twitter_handler','sanitize_twitter_handler');
```

```
function sanitize_twitter_handler($input){
		$output = sanitize_text_field($input); //converte simbolos para utf-8 entities 
		$output = str_replace('@','', $output);
		return $output;
}
```

Colocar uma descrição:
```
function sunset_sidebar_twitter(){
		$twitter = esc_attr(get_option('twitter_handler'));
		echo '<input type="text" name="twitter_handler" value="'.$twitter.'" placeholder="Twitter handler" />
		<p class="description">Input without @ </p>';
}
```