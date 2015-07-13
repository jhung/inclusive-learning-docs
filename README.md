# Doc-base Starter Content

This package includes sample content, styles, and navigation which you can
customize to create your own documentation site using Docpad.

# Get Started

1. Install DocPad: `sudo npm install -g docpad`
2. Get the node modules for this project: `npm install`
3. Generate the HTML. This will create output in the ./out/ directory: `docpad generate --env static`
4. Open the index.html located in the ./out/ directory in a web browser.

# Updating `doc-base`

Doc-base-start depends on the doc-base project. To update doc-base project,
you will need to:

1. Delete ./out/ directory
2. Delete ./node_modules/
3. Run `npm install`

# Deploy to GitHub Pages

```
docpad deploy-ghpages --env static
```

*Note:* The above command will deploy to the origin of the repository. To deploy
to production, you may need to be working from Master, not a fork.

# What is all this stuff?

- `/src/documents/*.md`  - the articles go here. Written in Markdown. By default populated with some placeholder documents.
- `/src/documents/css/*.css.styl` - CSS written in Stylus syntax goes in here.
- `/site-structure.json`  - the structure for navigation. By default has navigation for the placeholder content.
- `/src/layouts/default.html.handlebars` - the default content template for laying out the documents.
- `/src/ghpages-files/*`    - the 404 page, 404 styling, and gh-pages CNAME.
