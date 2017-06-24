## Adding a menu in the wordpress admin

Inside the theme folder, create the **admin** folder, inside that folder create a file called **function-admin.php**

This file should contain the following code:

```
function theme_add_menu_page(){
	//Add menu in admin
	add_menu_page(
		'<title></title>', //But it doesn't even seem like the one below overwrites
		'Nome no menu em si', //It has to be short so it doesn't get cut off in the responsive
		'manage_options', //permissão de admin
		'theme_menu_id', //id to know everything that will belong in this menu here
		'theme_create_page', //callback function, because wp is full of it
		'icone', //default is gear
		110 //menu order
	);
	
	//Add a submenu -> This first one is needed to put a different name in the submenu list
	add_submenu_page(
		'theme_menu_id', // Menu ID
		'<title></title>', // This is the browser tab title
		'Menu Name', // Should be short to prevent truncation in responsive layouts
		'manage_options', // Admin permission
		'theme_menu_id', // This is supposed to be the submenu's unique ID, but since we're overwriting, it should match the main menu ID. This parameter is repeated twice in this function.
		'theme_create_page' // The callback function, repeated exactly as in add_menu_page
	);
	}

	add_action('admin_menu', 'theme_add_menu_page'); // Calls the function we just wrote

	// Note: We must create the functions referenced in the callbacks, even if they're empty. Otherwise, it will throw an error.

	function theme_create_page() {
		// It can be empty, but if we use an echo with some HTML, it will appear on the page.
		echo '<h1>Theme Options</h1>';
	}
```
And don't forget, none of this will work unless you call this entire function in functions.php:

```
require get_template_directory() . '/admin/function-admin.php';
```