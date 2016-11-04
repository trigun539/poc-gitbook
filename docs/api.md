# API Standards

## Key requirements for the API

Many of the API design opinions found on the web are academic discussions revolving around subjective interpretations of fuzzy standards as opposed to what makes sense in the real world. My goal with this post is to describe best practices for a pragmatic API designed for today's web applications. I make no attempt to satisfy a standard if it doesn't feel right. To help guide the decision making process, I've written down some requirements that the API must strive for:

- It should use web standards where they make sense
- It should be friendly to the developer and be explorable via a browser address bar
- It should be simple, intuitive and consistent to make adoption not only easy but pleasant
- It should provide enough flexibility to power majority of the Enchant UI
- It should be efficient, while maintaining balance with the other requirements

Below is the standard the the EMR project will follow when creating backend APIs.

### Title

> The name of your API call

_Example: Show All Users_

- Note: try to use verbs that match both request type (fetching vs modifying) and plurality (one vs multiple.) 
- Note: Also add additional info here such as a description, if need be.

### URL

> The URL structure (path only, no root url)

```
/users
/users/:id
/users?search=Faye
```
- For fixed urls: /users or /photos
- For urls with parameters in them: /users/:id or /users?id=:id
