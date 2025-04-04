# contentful-migration

**Install contentful CLI globally**

```bash
npm install my-package
```
**Login & Log Out**
- Login via browser
  
```bash
contentful login
```

- Login via CMA Token

```bash
contentful login --management-token <management-token>
```

- Log Out

```bash
contentful logout
```
##

- Get a list of all available spaces

```bash
contentful space list
```

- MIgration

```bash
contentful space migration --space-id "[your-space-id]" --environment-id "[your-space-environment]" migration/demo.js -y
```

- Example of demo.js
<pre>
  module.exports = function (migration) {

  const blogPost = migration
    .createContentType("blogPost")
    .name("Demo Blog Post")
    .description("Blueprint for blog posts")
    .displayField("title");


  const title = blogPost.createField("title");
  title
    .name("Title")
    .type("Symbol")
    .required(true)
    .validations([{ unique: true }]);

  //   Post Author field
  const author = blogPost.createField("author");
  author.name("Author Name").type("Symbol").required(true).validations([]);

  //   Post body field
  const body = blogPost.createField("body");
  body.name("Body").type("RichText").required(true).validations([]);

};
</pre>






