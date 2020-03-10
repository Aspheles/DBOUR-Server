## DragonWindows

After years of hard work, reverse engineering, and team building we decided to release the AKCore server-side sources.
This hard work was accomplished by a team from different cultures, religions, and locations.
We successfuly passed over language barriers to make something that we are proud of, and happy to release to you today.
Special thanks to all the team members :heart:
  - SanGawku
  - Luizoe
  - Ebbo
  - Dumke
  - PurpleHeart
  - Arakjim
  
Also a huge thanks to all of the DBOUR team that supported us for all this time, even when we were away from the project.
And to you the community, without you this project may have never existed.

## Prerequisite

### Visual studio professional 2017
### Mysql mariadb 10.3.14 or greater (https://downloads.mariadb.org/)
### Mysql workbench or similar
### A brain ;)
### Git for windows

## Visual studio installation

Be sure you selected the same as describe:

![akcore](http://atidote63.free.fr/DBOInstall/1.PNG)

Then just 'next' 'next' 'next'

## Getting the repository

Once you installed and selected a nice theme to use on visual studio just create a folder where you want to clone the repository.
Get in the repository and shift-right click on it and select open powershell prompt.

![akcore](http://atidote63.free.fr/DBOInstall/2.PNG)

hit enter. (if a github login window prompt then log yourself..)

=> https://github.com/AK-Core/DragonWindows.git

Wait a bit untill the solution get downloaded (may to sometime depend on your internet connection)

![akcore](http://atidote63.free.fr/DBOInstall/3.PNG)

Once everything is done double click on DragonWindows.sln.

Now the solution is open, you need to get the nugget package back, right click ont the solution and select restore nugget package.

![akcore](http://atidote63.free.fr/DBOInstall/4.PNG)

Time to compile, right click on the solution one more time and 'BUILD'.

You should get it done depending on your configuration pretty quick without error if u followed the installation as i told u.

## Database installation

Run mariadb installation exe.

Hit Next.

Set a new root password, next.

next.

next.

install.

Open HeidiSQL that have been installed with mariadb.

Connect to your 127.0.0.1 database using your created root user.

Right click on the left panel and choose create new database:
![akcore](http://atidote63.free.fr/DBOInstall/5.PNG)

Then file => import sql file

Select:

\DragonWindows\Utils\SQL\dbo.sql

You'll need to add a new entry into gameserver table, and edit the realmlist table to fit it to your need (network).


## Running the server
Copy the following file into your build executable path (default is \DragonWindows\x64\Debug-Release):

\DragonWindows\Utils\TS

\DragonWindows\Utils\WorldData

\DragonWindows\DragonLib\mysql\lib\libmariadb.dll

\DragonWindows\Auth\Auth.json

\DragonWindows\Char\Char.json

\DragonWindows\Game\Game.json

Edit the configuration as you want to your specific mysql connection and such.

You should now be able to run Auth/Char/Game exe files without any trouble and log in game.

Exemple of a running Auth server:
![akcore](http://atidote63.free.fr/DBOInstall/6.PNG)
