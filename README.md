# Neat Starter

Starter Template for **N**etlify CMS, **E**leventy, **A**lpine JS & **T**ailwind CSS

## Live Demo

[https://neat-starter.netlify.app/](https://neat-starter.netlify.app/)

### Technologies used:

- [Netlify CMS](https://www.netlifycms.org/)
- [Eleventy](https://www.11ty.dev/)
- [Alpine.js](https://github.com/alpinejs/alpine)
- [Tailwind CSS](https://tailwindcss.com/)

If you want to use SASS, run the follwing command line code:

```
npm install sass --save-dev
```

And replace the exisiting scripts in package.json with these:

```
 "start": "npm-run-all --parallel eleventy browsersync watch:sass build:sass",
  "eleventy": "eleventy --watch",
  "debug": "set DEBUG=* & eleventy",
  "build": "cross-env NODE_ENV=production eleventy",
  "browsersync": "browser-sync start --server '_site' --files '_site' --port 8080 --no-notify --no-open",
  "watch:sass": "sass --watch src/static/sass:src/static/css",
  "build:sass": "sass src/static/sass:src/static/css"
```

For Tailwind, use the following:

```
 "start": "npm-run-all --parallel css eleventy browsersync",
  "eleventy": "eleventy --watch",
  "debug": "set DEBUG=* & eleventy",
  "css": "postcss src/static/css/tailwind.css --o _site/static/css/style.css --watch",
  "build": "cross-env NODE_ENV=production eleventy && cross-env NODE_ENV=production tailwindcss -i src/static/css/tailwind.css -o _site/static/css/style.css",
  "browsersync": "browser-sync start --server '_site' --files '_site' --port 8080 --no-notify --no-open"
```

| ![image](https://user-images.githubusercontent.com/1884712/93762662-a62e4700-fc2d-11ea-9b2c-fda9f503402b.png) |
| ------------------------------------------------------------------------------------------------------------- |

<a href="https://app.netlify.com/start/deploy?repository=https://github.com/surjithctly/neat-starter&amp;stack=cms"><img src="https://www.netlify.com/img/deploy/button.svg" alt="Deploy to Netlify" /></a>

## Getting Started

Detailed instructions are available in my blog. [Check it out](https://blog.surjithctly.in/neat-stack-create-a-static-website-with-netlify-cms-eleventy-alpinejs-and-tailwindcss)

[Netlify CMS Guide](https://www.netlifycms.org/docs/intro/)

### 1\. Clone this Repository

```
git clone https://github.com/surjithctly/neat-starter.git
```

### 2\. Navigate to the directory

```
cd neat-starter
```

### 3\. Install dependencies

```
npm install
```

### 4\. Build the project to generate the first CSS

This step is only required the very first time.

```
npm run build
```

### 5\. Run Eleventy

```
npm run start
```

### 6\. Run Netlify CMS Proxy Server

```
npx netlify-cms-proxy-server
```

## Author

Surjith S M ( [@surjithctly](https://surjithctly.in/) )
