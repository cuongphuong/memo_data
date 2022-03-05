---
id: 1646475727127
title: Deploy to Github page
category: Javascripts/ReactJS/
---

1. Cài đặt package gh-pages với lệnh sau

```
 npm install --save gh-pages
```
2. Update packag.json

```
// Thêm đường dẫn homepage
// https://[your-user-name].github.io/[your-repo-name]/
"homepage": "https://minhlq-0928.github.io/deploy-github/",

// Thêm command predeploy & deploy app
"predeploy": "npm run build",
"deploy": "gh-pages -d build",
```
3. Chạy deploy

```
npm run deploy
```
