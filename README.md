# shellscript_backupsysexternal_device01
backup system to usb by shellscript.  

[structure]
  1) .env: include log_dir path(test/production enviroment) and backup_dir path.  
  2) .gitignore: include .env to hide log_dir and backup_dir on github/gitlab.
  3) main.sh:  run this backupsystem via loading finctions from other scripts.
  4) log_manager.sh:  load log_dir from .env and set up each path via inputting command(test:sudo ./main.sh prod: sudo ENV=prod ./main.sh ).
  5) device_manager.sh: load backup_dir from .env and set up follow tastk
      1. check mount staus the device.
          if the device isn’t mounted show and record error message.
      2. execute backup date.
          send data to backup_dir.
          record the result of this system on log file.

