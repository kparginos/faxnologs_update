# FaxNoLogs Web App Container Update

<details><summary>Web App Current Version</summary>
<p>

>Web Application crrent version is v1.3.1

</p>
</details>

<details><summary>How to update the container on a host machine</summary>
<p>

1. Before updating the container you must download the following file:

  >* [FaxNoLogs-Containers-WinSetup.yml for Windows OS](https://github.com/kparginos/faxnologs_wepapp_update/blob/main/FaxNoLogs-Containers-WinSetup.yml)
  
</p>

<p>

2. To update to the latest version you need to do the following:

* For the Windows Host run this command:

```
docker-compose -f FaxNoLogs-Containers-WinSetup.yml pull
```

Once finished, run the following to update the web app container:

```
docker-compose -f FaxNoLogs-Containers-WinSetup.yml up -d
```


</p>
</details>

<details><summary>Bug fixes</summary>
<p>

* ### Web app version 1.2.3:

>1. When user presses the back button and the page to navigate to is then login screen, the system fires a logout command.

* ### Web app version 1.2.2:

>1. Sequence generator provided the same numbers when an admin re-initializes the counters. The fix provided checks the counters log to get the maximum log number and if it is greater than or equal to the current counter, increases the company's sequence generator counter to that number and returns the next one. If the admin sets the sequence generator counter to a value greater that the maximum log number then the sequense continues from that number.
		
</p>
</details>

<details><summary>Enhancements</summary>
<p>

* ### Web app version 1.3.1:
  Add logging to CounterService
  
* ### Web app version 1.3.0:

>1. A new user level has been added to the system in order to support the UnlockUsers admin user type
>2. A new menu item ***UnlockUsers*** has been created and it will be visible to all users under Admin and UnlockUsers levels. From this page an admin can unlock a user that had accidentally closed the browser without logging out. 

* ### Web app version 1.2.4:

>1. The session never times out for admins.

* ### Web app version 1.2.3:

>1. Two(2) filters added at the Counters History admin option to allow user to filter entries by Company ID and LogYear.
>2. When the application restarts(from Docker) all logged-in users will be logged-out automatically.

* ### Web app version 1.2.2:

>1. New option for the admins console to preview all counters history.

</p>
</details>
