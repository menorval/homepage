---
layout: build-errors
title: You are not currently logged in
image: /assets/social-cards/common-errors.png
description: You are not currently logged in
---

#### Error Message

> You are not currently logged in. To log in, use: $ serverless login


#### Problem

Serverless Framework tries to log you into your Serverless account when you have a Serverless organization specified in your `serverless.yml`:

``` yml
org: acme
service: notes

...
```

If the `org` is specified but you have not logged in to Serverless, you will get this error.

#### Solution

If you do not have a Serverless account, or want to skip the login step, you can simply comment out the `org` definition.

``` yml
# org: acme
service: notes
```

Alternatively, if you have a Serverless account, you can configure your Serverless token on Seed by [following our docs]({% link _docs/integrating-with-serverless-enterprise.md %}).