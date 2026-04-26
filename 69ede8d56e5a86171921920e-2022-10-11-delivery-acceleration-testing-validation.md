---
title: 'Delivery Acceleration: Testing & Validation'
subtitle: is testing enough to make sure our code works?
publishedAt: '2022-10-11T00:00:00.000Z'
coverImageUrl: 'https://www.alvarolorente.dev/img/blog/testing.jpg'
tags:
  - id: 56744723958ef13879b9550d
    name: Devops
    slug: devops
  - id: 56744721958ef13879b94a60
    name: Productivity
    slug: productivity
  - id: 56744721958ef13879b94c7e
    name: General Programming
    slug: programming
  - id: 6405b7ab024dffb6cd379ed5
    name: SoftwareDevelopment
    slug: softwaredevelopment
ogTitle: 'Delivery Acceleration: Testing & Validation'
ogDescription: is testing enough to make sure our code works?
ogImage: 'https://www.alvarolorente.dev/img/blog/testing.jpg'
coAuthors: []
---
Before we enable code for our clients, we need to test and validate it does what is expected. This could be an entire series of its own (please let me know if you want one), so I will keep it on a high level.

<!-- truncate -->

## Testing

I could probably spend hours sharing different types of testing strategies and where and why to use them.  
In reality, the most important thing, is to make sure we use the correct ratio of the different types of tests, as it will highly affect the time and location of your testing.

This ratio has always been shown as a pyramid with:

* **Unit test**: validate individual pieces of logic that are isolated.
* **Integration test**: validates interactions with multiple parts of your system or other systems.
* **Integrated test**: They test the system as a whole.

![](https://www.alvarolorente.dev/img/blog/pyramid.jpeg)

Tests are divided in these layers because there is a cost in time and complexity.

This affect the next DORA 4 metrics:

* ✔️ **Change Failure Rate**

## Validation

Validation differs from testing as it's the confirmation that the behavior is what the user expected, for now, humans are the only ones that can discern this.  
As we have seen in the previous chapter, the recommendation is to do this in production, so you get:

* Get real behaviors of interactions with other systems
* Get real performance

This affect the next DORA 4 metrics:

* ✔️ **Change Failure Rate**
