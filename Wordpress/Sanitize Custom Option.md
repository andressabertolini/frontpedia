## Sanitize Custom Option

```
register_setting('sunset-settings-group','twitter_handler','sanitize_twitter_handler');
```

```
function sanitize_twitter_handler($input){
		$output = sanitize_text_field($input); //convert symbols to utf-8 entities
		$output = str_replace('@','', $output);
		return $output;
}
```

Enter a description:
```
function sunset_sidebar_twitter(){
		$twitter = esc_attr(get_option('twitter_handler'));
		echo '<input type="text" name="twitter_handler" value="'.$twitter.'" placeholder="Twitter handler" />
		<p class="description">Input without @ </p>';
}
```