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

### Getting the Store id:

get store url without http

andressatests.myshopify.com

---

### Getting the Theme id:

Command > Get

theme get --list --password=you_api_password --store=your_store_id

You can also get it from the url when you click to customize the theme.

123936145598

---

### Indeed connecting the dots:

- - - ATTENTION: RUN THIS COMMAND INSIDE A FOLDER WHERE THE THEME WILL BE - - 

theme get --password=[your-api-password] --store=[your-store.myshopify.com] --themeid=[your-theme-id]

theme get --password=shppa_**************** --store=andressatests.myshopify.com --themeid=123936145598

theme watch 

To sync the changes