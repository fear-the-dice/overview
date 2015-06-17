#Lets Kill Things
A tool for helping manage combat in a turn based environment. Allowing DM's/GM's to control stats such as AC, HP, and damage taken for a group.


##Supervisor
Supervisor manages our various processes for us. If you don't already have it installed you can do so with the Python tool easy_install:

* **Installation:**

    ```
    $ easy_install supervisor
    ```    

* **Setup:**

   Replace *obihann* with your current username
   
   ```
   $ cp supervisor/supervisord.conf.example supervisor/supervisord.conf
   $ sed -i '' 's/USERNAME/obihann/g' supervisor/supervisord.conf
   ```

* **Use:**
    > Once you have it installed you can go ahead and run supervisor, then feed it some commands:

    ```
    $ sudo supervisord -c supervisor/supervisord.conf
    $ supervisorctl
    mongo                   STOPPED   Not started
    api                     STOPPED   Not started
    web                     STOPPED   Not started
    socket                  STOPPED   Not started
    supervisor> start mongo
    mongo: started
    supervisor> start api
    api: started
    supervisor> start socket
    socket: started
    supervisor> start web
    web: started
    supervisor>
    ```


##License
This tool is protected by the [GNU General Public License v2](http://www.gnu.org/licenses/gpl-2.0.html).

Copyright [Jeffrey Hann](http://jeffreyhann.ca/) 2015
