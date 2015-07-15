# Doc-base Starter Content

This package includes sample content, styles, and navigation which you can
customize to create your own documentation site using Docpad.

# Get Started Making a New / Custom Site

1. Clone the `doc-base` project: `git clone https://github.com/jhung/doc-base`
2. Clone the `doc-base-start` project into a custom directory: `git clone myProject https://github.com/jhung/doc-base-start`  (TODO: update this URL)
3. Change directories into myProject: `cd myProject`
4. Install DocPad if it isn't already installed: `sudo npm install -g docpad`
5. Get the required node modules: `npm install` (TODO: package.json looks for `doc-base` is in a sibling directory to `doc-base-start`. This should be fixed to use an URL for doc-base instead)
6. Generate the HTML. This will create output in the ./out/ directory: `docpad generate --env static`
7. Open the index.html located in the ./out/ directory in a web browser to confirm everything is working and to see the placeholder site.
8. You can now customize the site.

## Files You May Want to Customize for New Sites

- `/src/documents/*.md`  - the articles go here. Written in Markdown. By default populated with some placeholder documents.
- `/src/documents/css/*.css.styl` - CSS written in Stylus syntax goes in here.
- `/site-structure.json`  - the structure for navigation. By default has navigation for the placeholder content.
- `/src/layouts/default.html.handlebars` - the default content template for laying out the documents.
- `/src/ghpages-files/*`    - the 404 page, 404 styling, and gh-pages CNAME.

## Commiting Changes

When you are ready to commit changes, you will first need to change the local git repository's origin. We do this by:

1. renaming initial `origin` to `source`
2. add a new `origin` to reference the new site's repository.

Example:
```
git remote rename origin source
git remote add origin http://www.github.com/~your-project/your-repository/
git remote -v
```

Once this is done, you can commit to the new origin for your site.

# Updating `doc-base`

This project `doc-base-start` uses helper functions contained in the `doc-base` project. Periodically, doc-base will be updated.
To get the latest updates you will need to:

1. Delete ./out/ directory
2. Delete ./node_modules/
3. Run `npm install`

# Deploy to GitHub Pages

```
docpad deploy-ghpages --env static
```

*Note:* The above command will deploy to the origin of the repository. To deploy
to production, you may need to be working from Master, not a fork.
