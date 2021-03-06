# Commands


- ```-h``` or ```--help```  **—**  When this argument is passed, PyInstaLive's help message will be shown containing all available commands.

- ```-u``` or ```--username```  **—**  Instagram username to login with. Requires:  ```--password```, ```--download```.

- ```-p``` or ```--password```  **—**  Instagram password to login with. Requires:  ```--username```, ```--download```.

- ```-d``` or ```--download```  **—**  The username or user Id of the user whose livestream or replay you want to save.

- ```-r``` or ```--record```  **—**  The username of the user whose livestream or replay you want to save (legacy).

- ```-i``` or ```--info```  **—**  When this argument is passed, PyInstaLive will show information such as its current version, the configuration file contents, available cookie files and more.

- ```-nr``` or ```--noreplays```  **—**  When this argument is passed, PyInstaLive will not download any available replays. Overrides the configuration file.

- ```-nl``` or ```--nolives```  **—**  When this argument is passed, PyInstaLive will not download livestreams. Overrides the configuration file.

- ```-cl``` or ```--clean```  **—**  When this argument is passed, PyInstaLive clean the current download folder by deleting folders ending in `_downloads`. Any folders that contain a `folder.lock` file (e.g. folders for ongoing downloads) will be skipped.

- ```-df``` or ```--downloadfollowing```  **—**  When this argument is passed, PyInstaLive will check if any users from your following list have any available livestreams or replays and start a daemon process running PyInstaLive in the background for those that do. You cannot cancel the launched processes or start them with any extra arguments. It's recommended to enable ```log_to_file``` when using this argument. (Experimental, use at own risk.)

- ```-cp``` or ```--configpath```  **—**  Passing this argument along with a valid path to a different configuration file will override the default path.

- ```-sp``` or ```--saavepath```  **—**  Passing this argument along with a valid path to a different folder will override the path specified in the configuration file.



# Default configuration file

```ini
[pyinstalive]
username = johndoe
password = grapefruits
save_path = 
ffmpeg_path = 
show_cookie_expiry = true
clear_temp_files = false
save_lives = true
save_replays = true
run_at_start =
run_at_finish =
save_comments = false
log_to_file = false
use_locks = true
```

```username```  **—**  Instagram username to login with.

```password```  **—**  Instagram password to login with.

```save_path```  **—**  Path to the folder where downloaded Instagram livestreams and replays will be saved. PyInstaLive must have permission to write files to this folder. If left empty, PyInstaLive will attempt to fall back to the folder where it's being run from.

```ffmpeg_path```  **—**  User-defined path to the FFmpeg binary. If left empty, PyInstaLive will fall back to the system's environment variable.


```show_cookie_expiry```  **—**  When set to True, PyInstaLive will show when the current cookie used to login will expire.

```clear_temp_files```  **—**  When set to True, PyInstaLive will delete all temporary files that were downloaded as well as the folders which contained these files. Replay folders created by PyInstaLive will not be deleted because they are used to determine if a replay has already been downloaded.

```save_lives```  **—**  When set to True, PyInstaLive will download livestreams.

```save_replays```  **—**  When set to True, PyInstaLive will download any available replays.

```run_at_start```  **—**  Command to run when PyInstaLive starts downloading a livestream. Leave empty to disable. (Experimental, use at own risk.)

```run_at_finish```  **—**  Command to run when PyInstaLive finishes downloading a livestream. Leave empty to disable. (Experimental, use at own risk.) 
 
```save_comments```  **—**  When set to true, PyInstaLive will try to save comments from a livestream or replay to a log file. Verified users have *(v)* next to their name. (Experimental, use at own risk.)

```log_to_file```  **—**  When set to true, PyInstaLive will save all its console logs to a text file. The filename will be `pyinstalive_<live-username>.log` where `<live_username>` will be the username of the Instagram user whose livestream or replay you want to download. If no username was given to download (e.g when running `pyinstalive --clean`) the file will be named `pyinstalive.default.log`.

```save_comments```  **—**  When set to true, PyInstaLive will create several .lock files to prevent duplicate downloads from starting for the same user if you are running PyInstaLive using some form of automation such as batch/shell loops.
