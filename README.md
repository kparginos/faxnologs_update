# FaxNoLogs Web App Container Update

<details><summary>Installation Pre-requisities</summary>
<p>

- Please make sure you have apply previous updates ([FaxNoLogs Containers and Database Update](https://github.com/kparginos/faxnologs-dbupdate.git))
	
>### If you already have done it, **DO NOT RUN IT AGAIN !!!**

</p>
</details>

<details><summary>How to update the container on a host machine</summary>
<p>

1. Before updating the container you must download the following file depending on your OS:

  >* [FaxNoLogs-Containers-WinSetup.yml for Windows OS](https://github.com/kparginos/faxnologs_wepapp_update/blob/main/FaxNoLogs-Containers-WinSetup.yml)
  
  >* [FaxNoLogs-Containers-LinuxSetup.yml for Linux OS](https://github.com/kparginos/faxnologs_wepapp_update/blob/main/FaxNoLogs-Containers-LinuxSetup.yml)
  
</p>

<p>

2. To update to the latest version you need to do the following:

* For the Windows Host run this command:

```
docker-compose -f FaxNoLogs-Containers-WinSetup.yml pull
```

* For the Linux Host run this command:

```
docker-compose -f FaxNoLogs-Containers-LinuxSetup.yml pull
```

Once finished, run the following to update the web app container:

```
docker-compose -f FaxNoLogs-Containers-WinSetup.yml up -d --no-deps faxnologs_webapp
```


</p>
</details>

<details><summary>Bug fixes</summary>
<p>

* ### Web app version 1.2.2:

>1. Sequence generator provided the same numbers when an admin re-initializes the counters. The fix provided checks the counters log to get the maximum log number and if it is greater than or equal to the current counter, increases the company's sequence generator counter to that number and returns the next one. If the admin sets the sequence generator counter to a value greater that the maximum log number then the sequense continues from that number.
		
</p>
</details>

<details><summary>Enhancements</summary>
<p>

* ### Web app version 1.2.3:

>1. Two(2) filters added at the Counters History admin option to allow user to filter entries by Company ID and LogYear.
>2. When the application restarts(from Docker) all logged-in users will be logged-out automatically.

* ### Web app version 1.2.2:

>1. New option for the admins console to preview all counters history.

</p>
</details>
