## Scaffolding

any additional directories included in a theme are stripped out upon upload to Shopify

Assets
Assets contain all the assets used in the theme, including images, stylesheets, and JavaScript files.

Config
Config contains two JSON files to control the theme editor aka. the Customize Theme section of a Shopify store, allowing a developer to easily create theme options.

Layout
Layouts contains theme.liquid layout template; this template is usually the largest wrapper, and includes your header and footer.

Locales
Locales are used to provide translated content for the theme.

Sections
Sections are reusable modules of content that can be customized, dragged/dropped, and re-ordered by users of the theme.

Snippets
Snippets are bits of code that can be referenced in other Liquid template files within a theme. Use the Liquid include tag to load a snippet into your theme.

Templates
Templates contains all other Liquid templates, including those for customer accounts. Templates usually include snippets, and templates render in the  tag, found in the theme.liquid file.