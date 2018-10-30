# indexedDB
Simple encapsulation of indexedDB,Easy to use

- [Documentation](https://www.cnblogs.com/huangenai/p/9766453.html)

## important

```javascript
main.js
import db from "./indexedDB";

Vue.prototype.$db = db;
or
window.prototype.$db=db;

```


## Usage
``` javascript

 //Initialize the database
 this.$db.initDB();
 
 
 await this.$db.insert(this.$db.store.lang, item);
 
 this.$db.update(this.$db.store.token, {
              token: res.data.token,
              id: 1
 });
 
 await this.$db.clear(this.$db.store.lang);
 
 var getlang = await this.$db.get(this.$db.store.lang);
 or
 this.$db.get(this.$db.store.lang).then(res => {
    ....
});

this.$db.delete(this.$db.store.token, 1);
 
```

## important hint 

you must Initialize the database
``` javascript
 this.$db.initDB();
```
