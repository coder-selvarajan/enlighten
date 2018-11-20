# DOM Objects & Selectors

## Document object - basic things: 

```js
    let val;
      
    val = document.all[2];      //prints: <meta charset="UTF-8">
    val = document.all.length;  //prints: 43
    val = document.head;
    val = document.body;
    val = document.doctype;
    val = document.domain;
    val = document.URL;
    val = document.characterSet;
    val = document.contentType;
    val = document.forms;
    val = document.forms[0];
    val = document.forms[0].id;
    val = document.links;
    val = document.links[0];
    val = document.images;
    val = document.scripts;
    val = document.scripts[0].getAttribute('src');

    // loop thru document elements - sample
    let scripts = document.scripts;
    let scriptsArr = Array.from(scripts); //collection to array

    scriptsArr.forEach(function(script){
        //prints all the script file paths. 
        console.log(script.getAttribute('src')); 
    });

    console.log(val);
```

## DOM - Selectors:  (Single Element)
```js
    let val = document.getElementById('task-title');

    document.getElementById('task-title').style.background = '#333';
    document.getElementById('task-title').textContent = 'Task List';
    document.getElementById('task-title').innerText = 'My Task List';
    document.getElementById('task-title').innerHTML = '<b>My Task List</b>';

    var taskTitle = document.getElementById('task-title');
    taskTitle.innerHTML = '<b>My Task List</b>';

    console.log(val);
```

## DOM QuerySelector: (Single Element)
```js
    let val = document.getElementById('task-title');

    val = document.querySelector('#task-title');
    val = document.querySelector('.card-title');
    val = document.querySelector('h5');

    document.querySelector('li').style.color = 'red';
    document.querySelector('li:last-child').style.color = 'blue';
    document.querySelector('li:nth-child(3)').style.color = 'green';
    document.querySelector('li:nth-child(odd)').style.background = '#ccc';
    document.querySelector('li:nth-child(even)').style.background = '#fff';

    console.log(val);
```

## DOM - Selectors:  (Multiple Elements)
```js
    const items = document.querySelector('ul')
                          .getElementsByClassName('collection-item');
    // items will be the html collection here..
    items[4].style.color = 'red';
    console.log(items);

    let lis = document.querySelector('ul').getElementsByTagName('li');
    lis[2].style.color = 'red';

    // convert collection to array
    lis = Array.from(lis);
    lis.reverse();

    lis.forEach(function(li, index){
        console.log(li.className);
        li.textContent = `List-item ${index}`;
    });

    console.log(lis);
```

## DOM QuerySelectorAll: (Single Element)

```js
    const items = document.querySelectorAll('ul.collection li.collection-item');
    // items will be a Nodelist here.. It is not the html collection. 
    // so we dont need to convert it to array to loop it thru.. 
    items.forEach(function(item, index){
        item.textContent = `${index} : hello`;
    });

    const liOdd = document.querySelectorAll('li:nth-child(odd)');
    const liEven = document.querySelectorAll('li:nth-child(even)');
    liOdd.forEach(function(li, index){
        li.style.background = 'gainsboro';
    });

    for(let i=0; i<liEven.length; i++){
        liEven[i].style.background = 'whitesmoke';
    }
    console.log(items);
```
---

# Traversing the DOM: 

```js
    let val;
    const list = document.querySelector('ul.collection');
    const listItem = document.querySelector('li.collection-item:first-child');
    val = listItem;
    val = list;

    // Get child nodes
    val = list.childNodes;
    val = list.childNodes[0];
    val = list.childNodes[0].nodeName;

    // ChildNodes contain element textnode link comment etc.. 
    // 1 - Element
    // 2 - Attribute (deprecated)
    // 3 - Text node
    // 8 - Comment
    // 9 - Document itself
    // 10 - Doctype

    // Get children element nodes
    val = list.children;
    val = list.children[1];
    list.children[1].textContent = 'Hello';
    // Children of children
    list.children[3].children[0].id = 'test-link';
    val = list.children[3].children[0];
    // First child
    val = list.firstChild;
    val = list.firstElementChild;
    // Last child
    val = list.lastChild;
    val = list.lastElementChild;
    // Count child elements
    val = list.childElementCount;
    // Get parent node
    val = listItem.parentNode;
    val = listItem.parentElement;
    val = listItem.parentElement.parentElement;
    // Get next sibling
    val = listItem.nextSibling;
    val = listItem.nextElementSibling.nextElementSibling.previousElementSibling;
    // Get prev sibling
    val = listItem.previousSibling;
    val = listItem.previousElementSibling;
    console.log(val);
```

## Create Element: (with id, class, attributes, children)
```js
    // Create element
    const li = document.createElement('li');

    // Add class
    li.className = 'collection-item';

    // Add id
    li.id = 'new-item';

    // Add attribute
    li.setAttribute('title', 'New Item');

    // Create text node and append
    li.appendChild(document.createTextNode('Hello World'));

    // Create new link element
    const link = document.createElement('a');

    // Add classes
    link.className = 'delete-item secondary-content';

    // Add icon html
    link.innerHTML = '<i class="fa fa-remove"></i>';

    // Append link into li
    li.appendChild(link);

    // Append li as child to ul
    document.querySelector('ul.collection').appendChild(li);

    console.log(li);
```

## Removing & Replacing Elements: 
```js
    // REPLACE ELEMENT
    // Create Element
    const newHeading = document.createElement('h2');

    // Add id
    newHeading.id = 'task-title';
    // New text node
    newHeading.appendChild(document.createTextNode('Task List'));
    // Get the old heading
    const oldHeading = document.getElementById('task-title');

    //Parent
    const cardAction = document.querySelector('.card-action');

    // Replace
    cardAction.replaceChild(newHeading, oldHeading);

    // REMOVE ELEMENT
    const lis = document.querySelectorAll('li');
    const list = document.querySelector('ul');

    // Remove list item
    lis[0].remove();

    // Remove child element
    list.removeChild(lis[3]);

    // CLASSES & ATTR
    const firstLi = document.querySelector('li:first-child');
    const link = firstLi.children[0];
    let val;

    // Classes
    val = link.className;
    val = link.classList;
    val = link.classList[0];
    link.classList.add('test');
    link.classList.remove('test');
    val = link;

    // Attributes
    val = link.getAttribute('href');
    val = link.setAttribute('href', 'http://google.com');
    link.setAttribute('title', 'Google');
    val = link.hasAttribute('title');
    link.removeAttribute('title');
    val = link;
    console.log(val);
```
