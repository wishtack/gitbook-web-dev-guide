# Unit Testing

{% hint style="warning" %}
Unit-testing is **not optional** if you care about quality and your personal health.
{% endhint %}

{% hint style="success" %}
Unit testing improves teams **efficiency**, applications **quality** and **human lifespan**.
{% endhint %}

**Without automated tests:**

* every change is a challenge, 
* updating dependencies is too risky,
* refactoring is inacceptable,
* deployment is chaos,
* ...

{% hint style="success" %}
Modularity is unit testing's best friend.
{% endhint %}

## JavaScript Unit-Test Frameworks

### Jasmine

[https://jasmine.github.io/](https://jasmine.github.io/)

{% embed data="{\"url\":\"https://jasmine.github.io/\",\"type\":\"link\",\"title\":\"Jasmine Documentation\",\"icon\":{\"type\":\"icon\",\"url\":\"https://jasmine.github.io/favicon.ico\",\"aspectRatio\":0}}" %}

### Mocha

[https://mochajs.org/](https://mochajs.org/)

{% embed data="{\"url\":\"https://mochajs.org/\",\"type\":\"link\",\"title\":\"Mocha - the fun, simple, flexible JavaScript test framework\",\"icon\":{\"type\":\"icon\",\"url\":\"https://mochajs.org/static/favicon.copy.f17f048f84.ico\",\"aspectRatio\":0}}" %}

### Jest

[https://jestjs.io/](https://jestjs.io/)

{% embed data="{\"url\":\"https://jestjs.io/\",\"type\":\"link\",\"title\":\"Jest · 🃏 Delightful JavaScript Testing\",\"description\":\"🃏 Delightful JavaScript Testing\",\"icon\":{\"type\":\"icon\",\"url\":\"https://jestjs.io/img/favicon/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://jestjs.io/img/opengraph.png\",\"width\":796,\"height\":416,\"aspectRatio\":0.5226130653266332}}" %}

## Jasmine

### Example

```javascript
describe('priceScrapper', () => {

    let priceScrapper;
    
    beforeEach(() => priceScrapper = new PriceScrapper());

    it('should scrap prices without currency', () => {

        expect(priceScrapper.scrap('10.01')).toEqual({
            coefficient: 1001,
            currency: null,
            exponent: -2
        });

    });

    it('should scrap prices with currency', () => {

        expect(priceScrapper.scrap('$10.01')).toEqual({
            coefficient: 1001,
            currency: 'USD',
            exponent: -2
        });

    });

});
```

### Spies

Jasmine spies are mocks.

```javascript
describe('SearchEngine', () => {

    it('should pass locale to third party api', () => {

        /* Spying on `thirdPartySearchApi.search` and faking result. */
        spyOn(thirdPartySearchApi, 'search').and.returnValue([
            {
                title: 'Wishtack - Making Your Wishes Come True',
                url: 'https://www.wishtack.com'
            }
        ]);

        /* Trigger search. */
        searchEngine.search({keywords: 'Wishtack'});

        /* Check spy's call count. */
        expect(thirdPartySearchApi.search.callCount).toBe(1);

        /* Check spy's call args. */
        expect(thirdPartySearchApi.search).toHaveBeenCalledWith({
            country: 'US',
            keywords: 'Wishtack',
            language: 'en'
        });

    });

});
```

### Fetch Mock

If you are using `fetch` for HTTP requests, you can use `fetch-mock` to mock these http requests.

[http://www.wheresrhys.co.uk/fetch-mock/quickstart](http://www.wheresrhys.co.uk/fetch-mock/quickstart)

{% embed data="{\"url\":\"http://www.wheresrhys.co.uk/fetch-mock/quickstart\",\"type\":\"link\",\"title\":\"fetch-mock\",\"description\":\"Mock http requests made using fetch\",\"icon\":{\"type\":\"icon\",\"url\":\"http://www.wheresrhys.co.uk/favicon.ico\",\"aspectRatio\":0}}" %}



