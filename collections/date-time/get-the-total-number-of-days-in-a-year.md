---
title: Get the total number of days in a year
category: Date Time
tags:
  - posts
layout: layouts/post.njk
---

```js
const numberOfDays = year => (((year % 4 === 0) && (year % 100 !== 0)) || (year % 400 === 0)) ? 366 : 365;

// Or
const numberOfDays = year => new Date(year, 1, 29).getDate() === 29 ? 366 : 365;
```