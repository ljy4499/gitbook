# Web Cookies

Cookies is used in the browser since HTTP is stateless but we want to store the information on the HTTP interaction.

Client send cookies such as "Cookie: session.id=abc123123". Once Server receive cookies, verify the cookies, and it is validated, it send back "Set-Cookies: session.id=abc123123" to client.



<figure><img src=".gitbook/assets/image (1).png" alt="" width="343"><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

On  the web development tool from Chrome, we can see the cookie with the name and value of the cookie.  As the name of 'admin' was from my input as username, i don't know why the value is 'false'. It could be the key to get this cookie validated.



<div align="center">

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

</div>

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

After changing the cookie value, I re-entered the username and password to login this website. Boom! I was able to get in the website and obtained the flag.
