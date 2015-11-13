---
layout: post
title: Effective POM
---

So in the last post, I very briefly talked about Maven. As projects which use Maven for project management (or simply as a build tool) get bigger and more complex, one is bound to run into conflicts and issues.

Why is my project using the wrong version of this library?! :confused:

Or why is my project using this library in the first place? :tired_face:

To understand all that is being pulled into your project by the POM, it is often useful to see it's *effective POM*.

> The effective POM of a project is the final result of inheriting all parent POMs and super-POM defined within Maven, and interpolating them with project's POM, user-defined settings and active profiles.

To see the *effective POM* of your project, run the following CLI command:

```sh
mvn help:effective-pom
```
