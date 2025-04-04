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



<pre> ```bash git clone https://github.com/your-repo cd your-repo npm install ``` </pre>



