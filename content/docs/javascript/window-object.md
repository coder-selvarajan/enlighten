## Window object

In console type window. 
```js
    window.console.log("Hello")
    window.alert("Hello World");

    // prompt
    const input = prompt();
    alert(input);

    //confirm
    If (confirm("Are you sure?")){
        alert("proceed");
    }

    //window height
    alert(window.outerHeight);
    alert(window.outerWidth);

    //visible content area.. If firebug is open then the value change here..  
    alert(window.innerHeight); 
    alert(window.innerWidth);

    //scroll point
    window.scrollY;
    window.scrollX;
```

## Localtion Object
```js
    val = window.location
    console.log(val);
    //prints info related to http host info, protocol, 
    //query string, redirection etc.. 

    window.location.href="http://google.com";
```

## History Object
```js
    window.history.go(-1); //to navigate to previous page.. 
    val = window.history.length;
```

## Navigator Object
```js
    //display info about the browser..   
    //Appname, version, user agent, OS, language, vendor etc
    val = window.navigator;
```
