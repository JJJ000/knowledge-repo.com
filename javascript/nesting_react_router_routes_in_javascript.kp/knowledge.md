---
title: Creating routes within routes using react router version 4 or 5
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Nested routes in React Router v4/v5 are accomplished by nesting <Route> components within each other.
---

**Contents**

[TOC]

#### Defining Nested Routes
Nested routes are routes that are nested inside of other routes. For example, if a website has a page for a product, the product page may have a route for the product description, another route for product reviews, and another route for product specifications. All of these routes are nested inside of the product page route.

#### React Router v4 / v5
React Router v4 and v5 are popular routing libraries for React applications. React Router v4 provides a way to define nested routes in the same way as other routes. To define a nested route, you must first create a parent route and then add the nested routes as `children` of the parent route.

#### Example
For example, consider a React application with a route for a product page. The product page route has three nested routes, one for the product description, one for product reviews and one for product specifications.

```js
const App = () => (
  <Router>
    <Route path="/product" component={ProductPage}>
      <Route path="/product/description" component={ProductDescription} />
      <Route path="/product/reviews" component={ProductReviews} />
      <Route path="/product/specifications" component={ProductSpecifications} />
    </Route>
  </Router>
);
```

#### Rendering Nested Routes
In order to render the nested routes, you must define a `<Switch>` component inside of the parent route. The `<Switch>` component will render the first route that matches the current URL.

```js
const App = () => (
  <Router>
    <Route path="/product" component={ProductPage}>
      <Switch>
        <Route path="/product/description" component={ProductDescription} />
        <Route path="/product/reviews" component={ProductReviews} />
        <Route path="/product/specifications" component={ProductSpecifications} />
      </Switch>
    </Route>
  </Router>
);
```

With the `<Switch>` component in place, the React Router will render the appropriate nested route based on the current URL.
