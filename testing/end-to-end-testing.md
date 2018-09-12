# End-to-End Testing

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



