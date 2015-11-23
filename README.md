# RPG_Database

This database is aimed to be simple enough to show my understanding of SQL.

Make sure to read the comments.

It currently stores the SQL commands in text files.

makedb.text	creates the table structure
addcontent.text	adds the content based on the table structure

I have kept to a naming scheme to make SQL commands human readable.

I have tried to avoid using (too) platform specific SQL commands. I am not too bothered about which platforms it would work on as it would only require minor changes to the syntax.

# HOW TO

To make, on the commandline, run:

$ sqlite3.exe darkrpg < makedb.text
$ sqlite3.exe darkrpg < addcontext.text

To open, on the commandline, run:

$ sqlite3.exe darkrpg

I suggest entering the following SQLite commands first:

sqlite>.header on
sqlite>.mode column
sqlite>.timer on

Then, a complex SQL Query joining multiple tables:

SELECT Players.PlayerName, Characters.CharacterName, Weapons.WeaponName FROM Characters INNER JOIN Players ON Characters.PlayerID = Players.PlayerID INNER JOIN CharacterWeapons ON CharacterWeapons.CharacterID = Characters.CharacterID INNER JOIN Weapons ON CharacterWeapons.WeaponID = Weapons.WeaponID;

# Contact
Bertrand Brompton
bertrandbrompton@gmail.com
