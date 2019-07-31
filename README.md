# hackerrank_javascript

## Moonsoon Umberallas
```javascript
const biggerUmbrella = Math.max(...p)
    const remain = n % biggerUmbrella
    const peopleThatFit = Math.floor(n / biggerUmbrella)

    if (remain >= 1 && p.length === 1) {
        return -1
    } else {
        const remainingUmbrellas = p.filter(umbrella => umbrella !== biggerUmbrella)
        return remain !== 0 ? solve(remain, remainingUmbrellas) + peopleThatFit : peopleThatFit
    }
```
