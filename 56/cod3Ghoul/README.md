
Code Challenge 56 - Calculate the Duration of a Directory of Audio Files


The Challenge

Write a script that receives a directory name and retrieves all mp3 (or mp4 or m4a) files. It then sums up the durations of each file and prints them in a nice table with a total duration.

This could look like the following:

    $ module_duration.py ~/Music/iTunes/iTunes\ Media/Music/Manu\ Chao/Manu\ Chao\ -\ Esperanza/
    Manu Chao - Bixo.m4a                    : 112
    Manu Chao - Denia.m4a                   : 279
    Manu Chao - El Dorrado 1997.m4a         : 89
    Manu Chao - Homens.m4a                  : 198
    Manu Chao - Infinita Tristeza.m4a       : 236
    Manu Chao - La Chinita.m4a              : 93
    Manu Chao - La Marea.m4a                : 136
    Manu Chao - La Primavera.m4a            : 112
    Manu Chao - La Vacaloca.m4a             : 143
    Manu Chao - Le Rendez Vous.m4a          : 116
    Manu Chao - Me Gustas Tu.m4a            : 240
    Manu Chao - Merry Blues.m4a             : 216
    Manu Chao - Mi Vida.m4a                 : 152
    Manu Chao - Mr Bobby.m4a                : 229
    Manu Chao - Papito.m4a                  : 171
    Manu Chao - Promiscuity.m4a             : 96
    Manu Chao - Trapped by Love.m4a         : 114
    --------------------------------------------------
    Total                                   : 0:45:32


What will you learn?
Why do we think this is cool? There are a couple of subtasks here:
You learn how to do a common sysadmin task of listing files in a directory (check out the os, glob and pathlib modules).
You learn how to convert and calculate mm:ss (minutes/seconds) timings, which will hone your datetime skills.
As far as we know Python cannot extract audio meta data natively (yet), so you probably want to try a tool like FFmpeg (https://www.ffmpeg.org/) which is cool because then you need to know how to call an external command with Python and parse its output. You probably want to check out subprocess for this:
 The subprocess module allows you to spawn new processes, connect to their input/output/error pipes, and obtain their return codes. - docs (https://docs.python.org/3/library/subprocess.html)
