# Modify JavaScript



This problem is to win the lottery to get the flag. However, we have limited balance and tickets available by limited balance.&#x20;

<figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

From the source code, we can find the 'main.js' of this website. This JavaScript source code show us how this lottery system works. Since JavaScript handle user's input and send them to the server, we want to manipulate this javascript source code before it send to the server.

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

I copied main function of this lottery system to the web developer console and modified codes. Since 'cost' and 'ticket' variables was not defined, I changed them to integers.

```javascript
$.ajax({
  method : 'POST',
  url : '/purchase', 
  data : JSON.stringify({
  cost : 1,
  tickets : 10000000000000000
  }),
  dataType : 'json',
  contentType : 'application/json',
});
```



Once I send this data, I was able to gain the flag.

<figure><img src=".gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>



[https://www.youtube.com/watch?v=q2XAIR8lJ7w\&t=51s](https://www.youtube.com/watch?v=q2XAIR8lJ7w\&t=51s)
