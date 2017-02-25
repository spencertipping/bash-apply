# Convert imperative to functional commands
For example, I'd like a way to change my desktop background to a
brightness-adjusted copy of an image I have, but I don't want to store both
copies of the image. Ordinarily I'd write:

```sh
$ convert <args> adjusted.jpg
$ nitrogen --set-zoom-fill adjusted.jpg
$ rm adjusted.jpg
```

With bash-apply I'd write this:

```sh
$ apply 'nitrogen --set-zoom-fill' convert <args>
```
