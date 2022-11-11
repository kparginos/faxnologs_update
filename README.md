# FaxNoLogs Web App Container Update

<details><summary>Installation Pre-requisities</summary>
<p>

- Please make sure you have apply all previous updates up to version 1.2.1
	
>### If you already have done it, **DO NOT RUN IT AGAIN !!!**

</p>
</details><summary>Before update the container on a host machine</summary>
<p>
In order to update the container you must download the following file:

  1. [FaxNoLogs-Containers-WinSetup.yml for Windows OS](https://github.com/kparginos/faxnologs_wepapp_update/blob/main/FaxNoLogs-Containers-WinSetup.yml)
  2. FaxNoLogs-Containers-LinuxSetup.yml for Linux OS
  
</p>
<details>
</details>

<details><summary>How to update the container on a host machine</summary>
<p>

In order to update the latest containers you need to do the following:

* For the Windows Host run this command:

```
docker-compose -f FaxNoLogs-Containers-WinSetup.yml pull
```

* For the Linux Host run this command:

```
docker-compose -f FaxNoLogs-Containers-LinuxSetup.yml pull
```

Once finished run the following to update the web app container:

```
docker-compose -f FaxNoLogs-Containers-WinSetup.yml up -d --no-deps faxnologs_webapp
```


</p>
</details>
