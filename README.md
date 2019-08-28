# 🌹 @sharyn/hooks

## useStateObject

```jsx
import { useStateObject } from '@sharyn/hooks'
// or import useStateObject from '@sharyn/hooks/useStateObject'

const Cmp = () => {
  const { set: setField, get: getField, getAll: getFields } = useStateObject()

  return (
    <>
      <input
        name="firstname"
        onChange={e => setField('firstname', e.target.value)}
        value={getField('firstname') || ''}
      />
      <input
        name="lastname"
        onChange={e => setField('lastname', e.target.value)}
        value={getField('lastname') || ''}
      />
      <button onClick={() => console.log(getFields())}></button>
    </>
  )
}
```

### API

**`useStateObject(initialStateObject)`**: Pass an initial object to the hook, defaults to `{}`.

**`getAll()`**: Returns the entire state object

**`get(key)`**: Returns the value for the key

**`set(key, value)`**: Sets the value for the key

**`setAll(obj)`**: Replace the entire state object

**`del(key)`**: Deletes the value for the key

**`clear()`**: Resets the state object to `{}`

**`merge(obj)`**: Merge the state object deeply with an other object using Lodash's [merge](https://www.npmjs.com/package/lodash.merge).

**`assign(obj)`**: Merge the state object shallowly with an other object using `Object.assign()`.


## Credits

Hey, I am [@verekia](https://github.com/verekia) and this package is part of a library I am developing, [@sharynjs/sharyn](https://github.com/sharynjs/sharyn). The rest of the library is not ready to be used by the community.
