# Writing a PHP App
  
With Cloud9 IDE, you can run your PHP pages, without relying on a third-party system like Apache hosting. We run PHP version 5.3.3.

You can choose to run PHP scripts via the command line, by typing `php`, followed by the name of your PHP file. However, this is not a very common use case. Most likely, you'll be running your own server and hosting PHP files.
  
Here's a simple demonstration. First, create a PHP file called _hello_world.php_, and paste this code into it:
  
```html
<html>
  <head>
   <title>PHP Test</title>
  </head>
  <body>
   <?php echo '<p>Hello World</p>'; ?> 
  </body>
</html>
```

Next, open the **Run & Debug** panel, at the left of the IDE. From the **Runtime** dropdown, select **Apache+PHP**. Then, click on the ![The Run Button](./resources/icons/runButton.png) button in the top menu bar.
 
The console should now spit out a message about how your Apache server is running, something similar to this:
 
```no-highlight
Running Apache Process
Tip: you can access long running processes, like a server, at 'http://php_hello.gjtorikian.c9.io'.
```

Clicking on that link gets you to your PHP page. For a more in-depth workflow, see the article on [running WordPress entirely on Cloud9](./running_wordpress_on_cloud9.html).

## Modifying php.ini

You can configure your PHP installation by editing the `php.ini` located in the `/home/ubuntu/workspace` directory. Please note: in some cases `php.ini` is located somewhere else. Just create a simple PHP file running `phpinfo()` to find out where to look for `php.ini`.

Make sure to restart Apache after you have applied your changes

    apachectl restart

Note: Currently, you can't debug PHP applications yet, but we are working on adding this feature.
