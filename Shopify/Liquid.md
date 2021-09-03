## Produto

### Loop through product images

```
{% for image in product.images %}

<img src="{{ image |  img_url: 'medium' }}">

{% endfor %}
```

### Display the product title

```
<h2>{{product.title}}</h2>
```

### Check if the product is available

```
{% if product.available %}

<h2>Price: $99.99</h2>

{% else %}

<h2 class="sold-out">Sorry - sold out</h2>

{% endif %}
```

---

## Store

```
<div>{{ shop.description }}</div>
```

shop.enabled_payment_type**s**

The "s" at the end indicates a loop

--- 

## Filters
```
<p class="date-time">

{{ article.published_at | date : '%d %B %Y' }}

</p>
```

Find the asset path:
```
{{ 'style.css' | asset_url | stylesheet_tag }}
```

---

## Cart

### Items in the cart

```
{% if cart.item_count > 0 %}

<p>You have {{ cart.item_count }}

{{ cart.item_count | pluralize: 'item', 'itens' }} in your cart</p>

{% else %}

<p>There's nothing in your cart :( Why not have a <a href="/products">look at our product range</a></p>

{% endif %}
```