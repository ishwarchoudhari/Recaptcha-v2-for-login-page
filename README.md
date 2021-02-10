# reCAPTCHA V2 in Flask application for LOGIN PAGE 
use pip to install flask

```pip install flask``` 

## Recaptcha-v2-for-login-page
reCAPTCHA is a free service from Google that helps protect websites from spam and abuse. A “CAPTCHA” is a turing test to tell human and bots apart. It is easy for humans to solve, but hard for “bots” and other malicious software to figure out.By adding reCAPTCHA to a site, you can block automated software while helping your welcome users to enter with ease. Try it out at https://www.google.com/recaptcha/api2/demo.

pip install recaptcha

reCAPTCHA v2
Automatically render the reCAPTCHA widget
The easiest method for rendering the reCAPTCHA widget on your page is to include the necessary JavaScript resource and a g-recaptcha tag. The ```g-recaptcha``` tag is a DIV element with class name ```g-recaptcha``` and your site key in the ```data-sitekey``` attribute:

Automatically render the reCAPTCHA widget
The easiest method for rendering the reCAPTCHA widget on your page is to include the necessary JavaScript resource and a g-recaptcha tag. The ```g-recaptcha``` tag is a DIV element with class name g-recaptcha and your site key in the data-sitekey attribute:

```
<html>
  <head>
    <title>reCAPTCHA demo: Simple page</title>
    <script src="https://www.google.com/recaptcha/api.js" async defer></script>
  </head>
  <body>
    <form action="?" method="POST">
      <div class="g-recaptcha" data-sitekey="your_site_key"></div>
      <br/>
      <input type="submit" value="Submit">
    </form>
  </body>
</html>
```
The script must be loaded using the HTTPS protocol and can be included from any point on the page without restriction.

### Explicitly render the reCAPTCHA widget
Deferring the render can be achieved by specifying your onload callback function and adding parameters to the JavaScript resource.

1. Specify your ``` onload ``` callback function.  This function will get called when all the dependencies have loaded.

```<script type="text/javascript">
  var onloadCallback = function() {
    alert("grecaptcha is ready!");
  };
</script>
```
2. Insert the JavaScript resource, setting the onload parameter to the name of your onload callback function and the ```render``` parameter to ```explicit```.

```
<script src="https://www.google.com/recaptcha/api.js?onload=onloadCallback&render=explicit"
    async defer>
</script>
```
