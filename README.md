# CKeditor for DNN - Custom stuff
Lista CKeditor postavki za DNN

- Unutar "Editor Config" pretraži "StylesSet" i dodaj
```
[
    // Block Styles

    // Inline styles
    { name: 'Boja: Zelena',   element: 'span',    attributes: { 'class': 'color--primary' } },
    { name: 'Boja: Zlatna',   element: 'span',    attributes: { 'class': 'color--secondary' } }

    // Object Styles
]
```

- Unutar "Editor Config" pretraži "ExtraAllowedContent" i dodaj: [ref link](http://drupal.stackexchange.com/questions/90710/prevent-wysiwygckeditor-from-stripping-html-classes)
```
span;ul;li;table;td;style;*[id];*(*);*{*}
```

- Ako ne želi ispisivati span klase idi u "Editor Config" i izbriši iz "Protected Source"
```
( /<span class[\s\S]*?>[\s\S]*?<\/span>/gi )
```
