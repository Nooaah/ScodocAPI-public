# ScodocAPI

ScodocAPI is an API that allows you to retrieve your school grades (IUT Informatique Littoral Côte D'Opale Calais) thanks to your INE identifier.

## Documentation

**index.html :**
```html
<html lang="fr">
    <head>
        <title>Call Scodoc Nooaah's API</title>
        <script src='https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.min.js'></script>
        <script src="index.js"></script>
    </head>
    <body></body>
</html>
```

**index.js :**
```javascript
$(document).ready(function () {
    $.ajax({
        type: "POST",
        url: "https://scodoc.herokuapp.com/getData/",
        data: {
            ine: 'YourINEHere'
        },
        success: function (result) {
            console.log(result); //Return Object of the table : https://extra.univ-littoral.fr/abs/pt.php
        }
    });
});
```

**Format of the object :**
```javascript
var object = {
    tr: [{ //An Array of all tr in the table
        td: [] //An Array of all td in this tr
    }]
};
```

## Contributing

- [Nooaah](https://github.com/Nooaah)


## License
[MIT](https://choosealicense.com/licenses/mit/)
