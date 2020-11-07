# Getting started

```
$ npm init -y
Wrote to /Users/pclaerhout/Downloads/JonoFotografie/tailwindcss-tutorial/package.json:

{
  "name": "tailwindcss-tutorial",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
```

```
$ npm install tailwindcss
+ tailwindcss@1.9.6
added 92 packages from 90 contributors and audited 92 packages in 4.561s
```

```
$ npm install postcss
+ postcss@8.1.6
added 1 package and audited 188 packages in 1.5s
```

```
$ npm install postcss-cli
+ postcss-cli@8.2.0
added 84 packages from 66 contributors and audited 176 packages in 6.1s
```

```
$ npm install autoprefixer
+ autoprefixer@10.0.1
updated 1 package and audited 177 packages in 1.847s
```

```
$ npx tailwind init
  
   tailwindcss 1.9.6
  
   ✅ Created Tailwind config file: tailwind.config.js
  
```

Then create `postcss.config.js`:

```javascript
module.exports = {
    plugins: [
        require('tailwindcss'),
        require('autoprefixer'),
    ]
}
```

Then, create `css/tailwind.css`:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Update the `package.json` file:

```javascript
{
  "scripts": {
    "build": "postcss css/tailwind.css -o public/build/tailwind.css"
  }
}
```

The, try the build:

```
$ npm run build

> tailwindcss-tutorial@1.0.0 build /Users/pclaerhout/Downloads/JonoFotografie/tailwindcss-tutorial
> postcss css/tailwind.css -o public/build/tailwind.css

```

Install live-server for the previewing:

```
$ npm install -g live-server
/usr/local/bin/live-server -> /usr/local/lib/node_modules/live-server/live-server.js

> node install.js

  SOLINK_MODULE(target) Release/.node
  CXX(target) Release/obj.target/fse/fsevents.o
  SOLINK_MODULE(target) Release/fse.node
+ live-server@1.2.1
added 198 packages from 157 contributors in 21.061s
```

Preview your site:

```
$ live-server public
Serving "public" at http://127.0.0.1:8080
Ready for changes
GET /favicon.ico 404 1.969 ms - 150
```
