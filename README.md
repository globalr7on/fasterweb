# Fasterweb - Project 


# How we work with git

- ✅ Change to dev branch 
  ```git checkout dev```
- ✅ Create a new branch from dev. 
  ```git checkout -b nameOfBranch ```
- ✅ Add  your  change to  project
  ```git add . ```
- ✅ Document your changes 
  ```git  commit  -m "this is my maggic"```
- ✅ Merge your  changes to dev 
  ```git merge  origin  dev```
- ✅ Push the changes
  ```git push``` 
- ✅ Create Pull Request

  


# Using commit conventions
- ✅ Commit conventions 
    feat,  fix, style, chore
    chore(chat): add validation message



### Project structure

Inside AstroWind template, you'll see the following folders and files:

```
/
├── data/
|   └── blog/
|       ├── post-slug-1.md
|       ├── post-slug-2.mdx
|       └── ...
├── public/
│   ├── robots.txt
│   └── favicon.ico
├── src/
│   ├── assets/
│   │   ├── images/
|   |   └── styles/
|   |       └── base.css
│   ├── components/
│   │   ├── atoms/
│   │   ├── blog/
│   │   ├── core/
|   |   └── widgets/
|   |       ├── Header.astro
|   |       ├── Footer.astro
|   |       └── ...
│   ├── layouts/
│   |   |── BaseLayout.astro
│   |   └── ...
│   ├── pages/
│   |   ├── [...blog]/
|   |   |   ├── [...page].astro
|   |   |   └── [slug].astro
│   |   ├── [...categories]/
|   |   |   └── [category]/
|   |   |       └── [...page].astro
│   |   ├── [...tags]/
|   |   |   └── [tag]/
|   |   |       └── [...page].astro
│   |   ├── index.astro
|   |   ├── 404.astro
|   |   └-- rss.xml.js
│   ├── utils/
│   └── config.mjs
├── package.json
└── ...
```

### Commands

All commands are run from the root of the project, from a terminal:

| Command               | Action                                             |
| :-------------------- | :------------------------------------------------- |
| `npm install`         | Installs dependencies                              |
| `npm run dev`         | Starts local dev server at `localhost:3000`        |
| `npm run build`       | Build your production site to `./dist/`            |
| `npm run preview`     | Preview your build locally, before deploying       |
| `npm run format`      | Format codes with Prettier                         |
| `npm run lint:eslint` | Run Eslint                                         |
| `npm run astro ...`   | Run CLI commands like `astro add`, `astro preview` |

<br>

### Configuration

Basic configuration file: `./src/config.mjs`

```javascript
export const SITE = {
  name: 'Example',

  origin: 'https://example.com',
  basePathname: '/', // Change this if you need to deploy to Github Pages, for example
  trailingSlash: false, // Generate permalinks with or without "/" at the end

  title: 'Example - This is the homepage title of Example',
  description: 'This is the homepage description of Example',

  googleAnalyticsId: false, // or "G-XXXXXXXXXX",
  googleSiteVerificationId: false, // or some value,
};

export const BLOG = {
  disabled: false,
  postsPerPage: 4,

  blog: {
    disabled: false,
    pathname: 'blog', // blog main path, you can change this to "articles" (/articles)
  },

  post: {
    disabled: false,
    pathname: '', // empty for /some-post, value for /pathname/some-post
  },

  category: {
    disabled: false,
    pathname: 'category', // set empty to change from /category/some-category to /some-category
  },

  tag: {
    disabled: false,
    pathname: 'tag', // set empty to change from /tag/some-tag to /some-tag
  },
};
```

<br>

### Deploy

#### Deploy to production (manual)

You can create an optimized production build with:

```shell
npm run build
```

Now, your website is ready to be deployed. All generated files are located at
`dist` folder, which you can deploy the folder to any hosting service you
prefer.

<br>

## Roadmap

- _Project_:
  - Create simple and clear strategy to get template updates
- _Blog_:
  - Improve blog design
  - Create component or utilities for related posts
  - Add more _shortcodes_ or _embed_ functions to posts in Markdown: (eg video, tweet...)
- _More widgets_:
  - Add more Tailwind components useful for most scenarios (Features, Contact, Call to Actions, Content, FAQs ...)
  - Create external library or place with useful Tailwind components
- _More Examples_: Add commonly used example pages (Ex: About, Terms, Services...)
- _Documentation_: Create detailed documentation with best practices and redesign tips



<br>



