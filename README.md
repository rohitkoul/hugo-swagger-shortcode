# hugo-swagger-shortcode
========================

A [Hugo Shortcode](https://gohugo.io/extras/shortcodes/) to embed the Swagger Spec in a page. This repo is based on [swagger yaml tp html](https://gist.github.com/oseiskar/dbd51a3727fc96dcf5ed189fca491fb3) python script.

# Setup
========

Copy the following into your Hugo site's directory:

* `shortcodes/swagger-spec.html` to your `layouts/shortcodes` directory
* `swagger-css` dir to your `static/css/` directory
* `swagger-js` dir to your `static/js` directory

# Usage
=======
* Add `swagger-css/swagger-ui.css` to your site, e.g to your `layout/_default/baseof.html`
```
<link href="{{ "/css/swagger-css/swagger-ui.css" | relURL }}" rel="stylesheet" type="text/css">
```
* To embed the API documentation do the following:

```go
{{< swagger-spec url="local_or_remote_path_to_my_yaml_file"  >}}

# e.g.
{{< swagger-spec url="http://myexample.com:1313/swagger/api.yaml"  >}}

# or

{{< swagger-spec url="/swagger/api.yaml"  >}}

```

# Aside:
=======
 ** if you run into css issues, you could add a custom css as well. A sample of how to do that is added in `samples` directory.
 ** if your spec is not local to your server hosting the page or the server hosting the spec is not sending CORS headers, you may want to use a CORS proxy like `cors anywhere`


