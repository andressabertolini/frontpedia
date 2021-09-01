## Produto

### Loop pelas imagens do produto

{% for image in product.images %}

<img src="{{ image |  img_url: 'medium' }}">

{% endfor %}

### Exibir o título do produto

<h2>{{product.title}}</h2>

### Se o produto está disponível

{% if product.available %}

<h2>Price: $99.99</h2>

{% else %}

<h2 class="sold-out">Sorry - sold out</h2>

{% endif %}

---

## Loja

<div>{{ shop.description }}</div>

shop.enabled_payment_type**s**

- s no final indica um loop

--- 

## Filtros

<p class="date-time">

{{ article.published_at | date : '%d %B %Y' }}

</p>

achar o caminho do asset

{{ 'style.css' | asset_url | stylesheet_tag }}

---

## Carrinho

### Itens no carrinho

{% if cart.item_count > 0 %}

<p>You have {{ cart.item_count }}

{{ cart.item_count | pluralize: 'item', 'itens' }} in your cart</p>

{% else %}

<p>There's nothing in your cart :( Why not have a <a href="/products">look at our product range</a></p>

{% endif %}