---
layout: default
title: About
testo: cc va?
---
# About page

Ciao napo, bla bla....
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>{{ page.title }}</title>
  </head>
  <body>
    <h1>{{ "welcome to jetsouss resort!" | downcase }}</h1>
    <p>
        {{ page.testo }}
    </p>
  </body>
</html>
