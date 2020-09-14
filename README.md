![alt tag](https://travis-ci.com/Soldy/temprc.svg?branch=master)


# temprc

Simple temporally full block data storage for science calculation.



Example:

``` javascript
    const temprc = new (require('temprc')).temprc('tempdb');

    temprc.set('variable', {'test':'test string'});

    let data = temprc.get('variable');
    console.log(data.test);
    //    output : test string

```



Set variable :


``` javascript
    
    temprc.set(name, value);

```


Get variable :


``` javascript
    
    let out = temprc.get(name);
    // out = value

```

Check variable exist :


``` javascript
    
    let out = temprc.check(name);
    // out = true or false (boolean)

```

List all stored variable : 

```javascript

    let out = temprc.list();
    // out = [all variable name] (array)

```

Get all elements form the db:

```javascript
    let out = temprc.all();
    // out = object with all element
```

Remove an element:

```javascript

   let out = temprc.del(name);
   // out = true or false (boolean)
   
```

Force data save 

```javascript

   let out = temprc.save();
   
```

Setup autosave (enable/disable)

```javascript

   let out = temprc.setup('autosave', true or false);
   // default is : true
   
```

Setup hash (enable/disable)

```javascript

   let out = temprc.setup('hash', true or false);
   // default is : true
   
```



