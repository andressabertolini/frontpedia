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