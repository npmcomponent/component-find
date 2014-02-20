*This repository is a mirror of the [component](http://component.io) module [component/find](http://github.com/component/find). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-find`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# find

  Find the first matching value in an array.

## Installation

    $ component install component/find

## API

### find(array, fn)

  Find with a function:

```js
var tobi = find(users, function(u){ return u.name == 'Tobi' });
```

### find(array, string)

  Find with property strings:

```js
find(users, 'admin');
```

### find(array, object)

  Find with object value matching:

```js
var users = [];
users.push({ name: 'Tobi', age: 2, species: 'ferret' });
users.push({ name: 'Jane', age: 6, species: 'ferret' });
users.push({ name: 'Luna', age: 2, species: 'cat' });

find(users, { name: 'Jane', age: 6 });
// => { name: 'Jane', age: 6, species: 'ferret' }

find(users, { name: 'Jane', age: 1 });
// => undefined
```

# License

  MIT
