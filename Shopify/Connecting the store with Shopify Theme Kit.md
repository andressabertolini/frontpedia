## Connecting the store with Shopify Theme Kit

Acesse o Shopify Partners

https://partners.shopify.com/

- Crie uma loja de teste e certifique-se que tem um tema instalado

---

### Conseguindo o password:

Crie um custom app:

Clicando em Apps no menu e depois Private Apps

- nome: teste-themekit
- email
- Mudar permissão: Themes > Read and Write

Irá gerar o API Key e API Password (Shopify API credentials - Para conectar ao Shopify)

password: shppa_****************

---

### Conseguindo o Store id:

pegar a url da loja sem http

andressatests.myshopify.com

---

### Conseguindo o Theme id:

Command > Get

theme get --list --password=you_api_password --store=your_store_id

Também da pra pegar da url quando aperta pra customizar o tema

123936145598

---

### De fato conectando as pontas:

- - - ATENÇÃO: RODE ESSE COMANDO DENTRO DE UMA PASTA AONDE VAI FICAR O TEMA - - 

theme get --password=[your-api-password] --store=[your-store.myshopify.com] --themeid=[your-theme-id]

theme get --password=shppa_**************** --store=andressatests.myshopify.com --themeid=123936145598

theme watch 

Para syncar as mudanças