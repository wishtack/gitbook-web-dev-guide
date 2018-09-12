# Cross-Site Request Forgery

The access to a URL should not trigger implicit actions.

An attacker could craft a URL and maliciously **trigger the request from the victim's browser using implicitly the victim's credentials.**

This can be done using an `<img src="...">` tag on a malicious web site.

### Example

A URL like this `/hotels/123456/book?startDate=...` should not trigger booking...

**...** except if the URL contains a complex and unpredictable token which is verified by the backend.

