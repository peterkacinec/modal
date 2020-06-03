# Modal vue component for Laravel

## Installation

- doplnit do suboru composer.json
```
"require": {
    ...,
    "peterkacinec/modal": "@dev"
},
"repositories": [
    {
        "type": "vcs",
        "url": "https://github.com/peterkacinec/modal"
    }
],
```

- nasledne spustit prikaz `composer update`

## Nastavenie package

V cistej instalaci noveho projektu Laravel treba dodrzat tento postup:

- `laravel new NazovProjektu`
- `npm install`
- vo vasom projekte do suboru `resources/js/app.js` treba nalinkovat komponentu pridanim riadku `Vue.component('modal-component', require('../../vendor/peterkacinec/modal/src/ModalComponent').default);`
- spustit prikaz `npm run dev` alebo `npm run watch`

## Example

Priklad blade templatu

````

````
## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
