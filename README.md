# FaxNoLogs Web App Container Update

<details><summary>Installation Pre-requisities</summary>
<p>

- Please make sure you have apply all previous updates up to version 1.2.1
	
>### If you already have done it, **DO NOT RUN IT AGAIN !!!**

</p>
</details>

<details><summary>How to update the container on a host machine</summary>
<p>

1. Before update the container you must download the following file depending on your OS:

  >* [FaxNoLogs-Containers-WinSetup.yml for Windows OS](https://github.com/kparginos/faxnologs_wepapp_update/blob/main/FaxNoLogs-Containers-WinSetup.yml)
  
  >* [FaxNoLogs-Containers-LinuxSetup.yml for Linux OS](https://github.com/kparginos/faxnologs_wepapp_update/blob/main/FaxNoLogs-Containers-LinuxSetup.yml)
  
</p>

<p>

2. To update to the latest container you need to do the following:

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
