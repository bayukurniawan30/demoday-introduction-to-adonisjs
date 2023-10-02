---
theme: purplin
class: text-center
highlighter: prism
lineNumbers: true
info: |
  ## Taksu Demo Day 58
drawings:
  persist: false
title: Introduction to AdonisJS
---

<div class="w-full flex items-center justify-center">
  <img src="/img/adonisjs-logo.png" class="h-20 mb-8" />
</div>

## Introduction to AdonisJS

Taksu Demo Day #58

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Next <carbon:arrow-right class="inline"/>
  </span>
</div>

<BarBottom  title="Taksu Demo Day #58">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>


---

# What is AdonisJS?

<style>
  .general-desc {
    line-height: 2rem !important;
  }
</style>

<div v-click class="text-2xl text-white mt-10">
<p class="general-desc">
AdonisJS is a fully featured web framework for Node.js. It has everything you need to create a fully functional web app or an API server.</p>

<p class="general-desc">
It also has built-in authentication, validator, template engine, ORM, and CLI command.
</p>

<p class="general-desc">
Some people say it's a Nodejs version of Laravel.
</p>

</div>

<BarBottom  title="Taksu Demo Day #58">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

<!-- 
Put comment here
-->

---

# Why AdonisJS?

<div v-click class="text-2xl text-white mt-10">- MVC Architecture</div>
<div v-click class="text-2xl text-white mt-3">- Typescript support</div>
<div v-click class="text-2xl text-white mt-3">- Robust ORM</div>
<div v-click class="text-2xl text-white mt-3">- Well written documentation</div>
<div v-click class="text-2xl text-white mt-3">- Built-in tests</div>
<div v-click class="text-2xl text-white mt-3">- Multi storage driver support</div>
<div v-click class="text-2xl text-white mt-3">- Multi auth driver support</div>

<BarBottom  title="Taksu Demo Day #58">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

<!--  
Put comment here
-->

---

# Routing


<div class="text-2xl text-white mt-10">
Below is the example of basic routing in AdonisJS
</div>

```ts {3-5}
import Route from '@ioc:Adonis/Core/Route'

Route.get('/', () => {
  return 'Hello world'
})

```

<div class="text-2xl text-white">or</div>

```ts {3-5}
import Route from '@ioc:Adonis/Core/Route'

Route.get('posts', 'PostsController.index')

```

<BarBottom  title="Taksu Demo Day #58">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

<!--
Put comment here
-->

---

# Model

<div class="text-2xl text-white mt-10">
Below is the example of model in AdonisJS
</div>

```ts {4-21}
import { DateTime } from 'luxon'
import { BaseModel, column } from '@ioc:Adonis/Lucid/Orm'

export default class User extends BaseModel {
  @column({ isPrimary: true })
  public id: number

  @column()
  public username: string

  @column()
  public email: string

  @column({ serializeAs: null })
  public password: string

  ...
}
```

<BarBottom  title="Taksu Demo Day #58">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

---

# Controller

<div class="text-2xl text-white mt-10">
Below is the example of controller in AdonisJS
</div>

```ts {4-9}
import { HttpContextContract } from '@ioc:Adonis/Core/HttpContext'
import Post from 'App/Models/Post'

export default class PostsController {
  public async index(ctx: HttpContextContract) {
    const posts = Post.query().paginate(1, 10)
    return response.status(200).json(posts)
  }
}
```

<div class="text-2xl text-white mt-10">
AdonisJS also support resource controller.
</div>

<BarBottom  title="Taksu Demo Day #58">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

---

# Templating Syntax

<div class="text-2xl text-white mt-10">
AdonisJS use Edge as templating engine. The syntax is almost similar to Blade in Laravel.
</div>

```ts {1|3-5|7-9|11}
{{ user.name }}

@if(condition)
  ...
@end

@each(post in posts)
  <li> {{ post.title }} </li>
@end

@include('partials/header')

```

<BarBottom  title="Taksu Demo Day #58">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

---

# Pros and Cons

<div v-click class="text-2xl text-white mt-10">
Pros:
</div>
<div v-click class="text-2xl text-white mt-3">- Productivity</div>
<div v-click class="text-2xl text-white mt-3">- MVC architecture</div>
<div v-click class="text-2xl text-white mt-3">- Robust ORM</div>

<div v-click class="text-2xl text-white mt-10">
Cons:
</div>
<div v-click class="text-2xl text-white mt-3">- Learning curve</div>
<div v-click class="text-2xl text-white mt-3">- Not as Popular as other framework</div>
<div v-click class="text-2xl text-white mt-3">- Community Size</div>


<BarBottom  title="Taksu Demo Day #58">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

---

# What's Next?

<div v-click class="text-2xl text-white mt-10">
Next demo day, will be a coding session about CRUD Controller with AdonisJS. So don't miss it!
</div>
