# GATSBY MDX BLOG

## Project Setup

1. Base - Gatsby Starter
2. Components + Imports - ready
3. main.css + styled components
4. constants (different setup)
5. Complete React Components for MDX

## Boring Components

0. Home Page
1. Navbar
2. Sidebar
3. Hero
4. Footer
5. Error Page
6. Newsletter

```html
<form
  className="contact-form"
  name="contact"
  method="post"
  netlify-honeypot="bot-field"
  data-netlify="true"
  action="/success"
>
  <input type="hidden" name="bot-field" />
  <input type="hidden" name="form-name" value="contact" />
</form>
```

7. Success Page (optional);

## Basic MDX Setup

1. Install mdx plugin
2. Add `gatsby-plugin-mdx` to gatsby-config
3. Setup Page - pageName.mdx /pages
4. Basic Markdown
5. Add React Components including Gatsby Link
6. Basic Styling
7. New Line Gotcha

## Multiple Posts

1. Setup Posts Folder
2. Add New filesystem Instance to gatsby-config

```js
{
      resolve: `gatsby-source-filesystem`,
      options: {
        name: `posts`,
        path: `${__dirname}/src/posts`,
      },
    },

```

4. Create a Brand New Folder For Post
   Won't Query Name - setup is up to you
5. Add mdx file
6. DOUBLE CHECK PATHS (../../ - gotcha)
7. Run 'gatsby clean' - just to be on the safe side
8. Seperate Images Folder
9. FrontMatter (space gotcha - title: first post)
10. Imports after FrontMatter

## Create MDX Pages Programatically

1. Setup Query with unique value (most likely slug)
2. Setup Template
3. Run Query in gatsby-node.js - just like normal setup
4. Pass Variable (slug)
5. Run Query in Template using variable (slug)

## Add INLINE Images to MDX

1. Syntax - ![](./pathToImages/imageName - if in the same folder)
2. Install - gatsby-transformer-remark
3. Changes in gatsby config

   remove - 'gatsby-plugin-mdx'
   add

```js
{
      resolve: `gatsby-plugin-mdx`,
      options: {
        gatsbyRemarkPlugins: [{ resolve: "gatsby-remark-images" }],
      },
    },
```

4. Restart the server
5. Whitespace gotchas and "gatsby clean"
6. Styling - Good Luck!

## Videos

### Reg Video

1. The same as regular video
2. autoPlay - gotcha
3. use like regular component

### Iframe

1. Gatsby Docs
2. Gotchas - url, styling
3. Use in template - johnsmilga.com

### MDX

[MDX Reference] : https://mdxjs.com/getting-started

[ Elements Reference] : https://www.gatsbyjs.org/docs/mdx/customizing-components/
