# End to End Testing

By definition, unit-tests **don't test interactions between modules** and some side-effects.

The whole application **must also be tested automatically**.

## Protractor

Protractor is an e2e _\(end-to-end\)_ testing framework developed by the AngularJS team.

It can test AngularJS or Angular web applications but also **non-AngularJS web applications**.

Protractor uses the Selenium webdriver to communicate with browsers and control them.

Protractor tests are written in **JavaScript** _**\(or TypeScript\)**_ **with Jasmine**.

```javascript
describe('angularjs homepage todo list', () => {

    it('should add a todo', () => {
    
        browser.get('https://angularjs.org');

        /* Add an element. */
        element(by.model('todoList.todoText')).sendKeys('write first protractor test');
        element(by.css('[value="add"]')).click();

        /* Check todo list content. */
        const todoList = element.all(by.repeater('todo in todoList.todos'));
        expect(todoList.count()).toEqual(1);
        expect(todoList.get(0).getText()).toEqual('write first protractor test');

    });

});
```

{% hint style="success" %}
**Page objects:**

Factorize each view's _\(or page\)_ logic in a dedicated and **reusable class** _\(separation of concerns\)_.
{% endhint %}

```javascript
import { PageTodo } from './pages/page-todo';

describe('angularjs homepage todo list', () => {

    it('should add a todo', () => {

        const pageTodo = new PageTodo();
    
        browser.get(pageTodo.pageUrl());

        /* Add an element. */
        pageTodo.addTodo({title: 'write first protractor test'});

        /* Check todo list content. */
        const todoElementList = pageTodo.todoElementList();

        expect(todoElementList.count()).toEqual(1);
        expect(todoElementList.get(0).getText()).toEqual('write first protractor test');

    });

});
```

## Cross-Browser & Cross-Device Test Automation with Browserstack

Browserstack is a cloud service with a large set of remotely controllable devices and browsers.

With Browserstack, you can run your Protractor tests on mobile and desktop.

[https://www.browserstack.com](https://www.browserstack.com)

{% embed data="{\"url\":\"https://www.browserstack.com\",\"type\":\"link\",\"title\":\"The Most Reliable Web & Mobile App Testing Platform\",\"description\":\"Instant access to 1200+ browsers and real iOS and Android devices. Ship mobile apps and websites that work for everyone, every time. Get Free Trial\",\"icon\":{\"type\":\"icon\",\"url\":\"https://3fxtqy18kygf3on3bu39kh93-wpengine.netdna-ssl.com/wp-content/themes/browserstack/img/favicons/apple-touch-icon.png\",\"width\":160,\"height\":160,\"aspectRatio\":1}}" %}

Browserstack records logs, captures screenshots and records testing videos.

{% hint style="info" %}
Apps can also be tested manually on Browserstack.
{% endhint %}

{% hint style="info" %}
You can open a tunnel with Browserstack to test locally hosted applications.
{% endhint %}

## Cypress

Cypress is another JavaScript End to End Testing Framework.

[https://www.cypress.io/](https://www.cypress.io/)

{% embed data="{\"url\":\"https://www.cypress.io/\",\"type\":\"link\",\"title\":\"JavaScript End to End Testing Framework \| Cypress.io\",\"description\":\"Fast, easy and reliable testing for anything that runs in a browser. Install Cypress in seconds and take the pain out of front-end testing.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.cypress.io/img/favicon.ico\",\"width\":16,\"height\":16,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://www.cypress.io/img/cypress-io-logo-social-share.png\",\"width\":1200,\"height\":628,\"aspectRatio\":0.5233333333333333}}" %}

## Takeaways

### Cross-Browser & Cross-Device E2E Testing Automation Blog Post

[https://blog.wishtack.com/2015/05/07/cross-browser-testing-test-automation-with-protractor-and-browserstack/](https://blog.wishtack.com/2015/05/07/cross-browser-testing-test-automation-with-protractor-and-browserstack/)

{% embed data="{\"url\":\"https://blog.wishtack.com/2015/05/07/cross-browser-testing-test-automation-with-protractor-and-browserstack/\",\"type\":\"link\",\"title\":\"Cross Browser Testing & Test Automation with Protractor and Browserstack\",\"description\":\"Cross-Browser Testing, what’s that for? Did you just come up with this new brilliant web app idea and you are now wondering how to make sure it works on all devices? or do you already have an…\",\"icon\":{\"type\":\"icon\",\"url\":\"https://wishtackblog.files.wordpress.com/2017/03/cropped-wishtack\_logo\_1024x1024.png?w=192\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://wishtackblog.files.wordpress.com/2017/03/cross-browser-testing.png?w=640\",\"width\":583,\"height\":437,\"aspectRatio\":0.7495711835334476}}" %}

### "Boilerplate" to run your first protractor tests

[https://github.com/wishtack/wt-protractor-boilerplate](https://github.com/wishtack/wt-protractor-boilerplate)

{% embed data="{\"url\":\"https://github.com/wishtack/wt-protractor-boilerplate\",\"type\":\"link\",\"title\":\"wishtack/wt-protractor-boilerplate\",\"description\":\"A boilerplate to run e2e tests using gulp, protractor and browserstack on AngularJS and non-AngularJS web apps. - wishtack/wt-protractor-boilerplate\",\"icon\":{\"type\":\"icon\",\"url\":\"https://github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars3.githubusercontent.com/u/7060848?s=400&v=4\",\"width\":128,\"height\":128,\"aspectRatio\":1}}" %}

### Useful modules

[https://github.com/wishtack/wt-protractor-runner](https://github.com/wishtack/wt-protractor-runner)

{% embed data="{\"url\":\"https://github.com/wishtack/wt-protractor-runner\",\"type\":\"link\",\"title\":\"wishtack/wt-protractor-runner\",\"description\":\"Gulp task to run multiple protractor configurations sequentially, useful for cross-browser testing - wishtack/wt-protractor-runner\",\"icon\":{\"type\":\"icon\",\"url\":\"https://github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars3.githubusercontent.com/u/7060848?s=400&v=4\",\"width\":128,\"height\":128,\"aspectRatio\":1}}" %}

[https://github.com/wishtack/wt-protractor-utils](https://github.com/wishtack/wt-protractor-utils)

{% embed data="{\"url\":\"https://github.com/wishtack/wt-protractor-utils\",\"type\":\"link\",\"title\":\"wishtack/wt-protractor-utils\",\"description\":\"Protractor utils to help you generate capabilities configuration for platforms like browserstack. - wishtack/wt-protractor-utils\",\"icon\":{\"type\":\"icon\",\"url\":\"https://github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars3.githubusercontent.com/u/7060848?s=400&v=4\",\"width\":128,\"height\":128,\"aspectRatio\":1}}" %}

