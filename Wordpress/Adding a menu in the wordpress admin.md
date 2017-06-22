## Adding a menu in the wordpress admin

Inside the theme folder, create the **admin** folder, inside that folder create a file called **function-admin.php**

This file should contain the following code:

```jsx
function theme_add_menu_page(){
	//Adiciona o menu no admin
	add_menu_page(
		'<title></title>', //Mas nem aparece pq o de baixo sobreescreve
		'Nome no menu em si', //Tem que ser curto pra não cortar no responsivo
		'manage_options', //permissão de admin
		'theme_menu_id', //id pra saber tudo que vai pertencer nesse menu aqui
		'theme_create_page', //função de callback, pq o wp é cheio disso
		'icone', //o padrão é a engrenagem
		110 //ordem do menu
	);
	
	//Adiciona um submenu -> Esse primeiro é necessário pra colocar um nome diferente na lista de submenus
	add_submenu_page(
		'theme_menu_id', //id do menu
		'<title></title>', //Fica na abinha do navegador
		'Nome no menu em si', //Tem que ser curto pra não cortar no responsivo
		'manage_options', //permissão de admin
		'theme_menu_id', //Esse era pra ser o id próprio do submenu, mas como vamos sobreescrever, esse é igual ao do menu de cima, repete mesmo esse parametro duas vezes aqui nessa função
		'theme_create_page' //A função também repete igualzinho a do add_menu_page
	);
}

add_action('admin_menu','theme_add_menu_page'); //chama toda essa função que escrevemos

//Atenção, temos que criar as funções que chamamos nos callbacks mesmo que estejam vazias, senão dá erro

function theme_create_page(){
	//Pode estar vazia, mas se a gente chamar um echo com um htmlzinho, vai aparecer dentro da página
	echo '<h1>Theme Options</h1>';
}
```

Agora, nada disso vai funcionar se você não chamar essa função toda no functions.php
```
require get_template_directory(). '/admin/function-admin.php';
```