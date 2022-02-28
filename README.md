# nuRL

Extends URL parsing to include .tld information and heuristics to extract data from the path and query. 

## pro-nounce

`nu-RL`

## examples

```js
nuRL('https://example.com/products/12345?alpha=xyz&gamma=abbbcaddeffff&beta=1324-234484-12323-12')

/*

{
  ...normalURLfields,
  productID: 12345,
  name: 'example'
  tld: '.com',
  alpha: 'xyz',
  beta: {
    type: 'uuid',
    value: '...."
  },
  gamma: {
    type: 'base64-json',
    value: {
      hi: 1
    }
  }
}
```

seems fun
