# Commands


- ```-h``` or ```--help```  **—**  When this flagis passed, PyInstaLive's help message will be shown containing all available flags and arguments.

- ```-u``` or ```--username```  **—**  Instagram username to login with. Requires:  ```--password```, ```--record```.

- ```-p``` or ```--password```  **—**  Instagram password to login with. Requires:  ```--username```, ```--record```.

- ```-r``` or ```--record```  **—**  The username of the user whose livestream or replay you want to save.

- ```-i``` or ```--info```  **—**  When this flag is passed, PyInstaLive will show information such as its current version, the configuration file contents, available cookie files and more.

- ```-nr``` or ```--noreplays```  **—**  When this flag is passed, PyInstaLive will not check for any available replays. Overrides the configuration file.


# Configuration file

```ini
[pyinstalive]
username = johndoe
password = grapefruits
save_path = 
show_cookie_expiry = true
clear_temp_files = false
save_replays = true
```

```username```  **—**  Instagram username to login with.

```password```  **—**  Instagram password to login with.

```save_path```  **—**  Path to the folder where downloaded Instagram livestreams and replays will be saved. (Requires write permissions)

```show_cookie_expiry```  **—**  When set to True, PyInstaLive will show when the current cookie used to login will expire.

```clear_temp_files```  **—**  When set to True, PyInstaLive will delete all temporary files that were downloaded. Folders created by PyInstaLive will not be deleted.

```save_replays```  **—**  When set to True, PyInstaLive will check for and download any available replays.