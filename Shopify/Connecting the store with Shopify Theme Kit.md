## Connecting the store with Shopify Theme Kit

Access Shopify Partners

https://partners.shopify.com/

- Create a test store and make sure you have a theme installed

---

### Getting the password:

Create a custom app:

Clicking on Apps in the menu and then Private Apps

- name: test-themekit
- email
- Change permission: Themes > Read and Write

It will generate the API Key and API Password (Shopify API credentials - To connect to Shopify)

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