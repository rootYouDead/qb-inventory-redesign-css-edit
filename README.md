# qb-inventory redesign css edit
Discord: https://discord.gg/6zxH7NdaTn
Normal qb-inventory görüntüsü kötü olduğunu düşündüğüm için yeni bir css ve para ve karakter isim soyisim eklentisi yaptık 
beğenirseniz iyi kullanımlar dileriz. 
Discord adresimize katılarak sorununuz varsa sorunuza yardımcı olmaya çalışırız.
---------------------------------------------------------------------------------
Since I think the normal qb-inventory visual is bad, we made a new css and money and character name surname plugin, 
if you like it, we wish you good use. If you have a problem, we will try to help you with your question by joining our Discord address.
## Screenshot
![image](https://github.com/user-attachments/assets/ee75e80c-ca02-4db5-9039-5c6f7a5946e8)
![image](https://github.com/user-attachments/assets/de12c3f1-0682-4355-a803-30344b507fc1)

## Dependencies
- [qb-core](https://github.com/qbcore-framework/qb-core)
- [qb-smallresources](https://github.com/qbcore-framework/qb-smallresources) - For logging transfer and other history

## Features
- Stashes (Personal and/or Shared)
- Vehicle Trunk & Glovebox
- Weapon Attachments
- Shops
- Item Drops

## Documentation
https://docs.qbcore.org/qbcore-documentation/qbcore-resources/qb-inventory

## Installation
### Manual
- Download the script and put it in the `[qb]` directory.
- Import `qb-inventory.sql` in your database
- Add the following code to your server.cfg/resouces.cfg

# Migrating from old qb-inventory

## Database
### Upload the new `inventory.sql` file to create the new `inventories` table
### Use the provided `migrate.sql` file to migrate all of your saved inventory data from stashes, trunks, etc
### Once complete, you can delete `gloveboxitems` `stashitems` and `trunkitems` tables from your database
```sql
CREATE TABLE IF NOT EXISTS `inventories` (
  `id` INT(11) NOT NULL AUTO_INCREMENT,
  `identifier` VARCHAR(50) NOT NULL,
  `items` LONGTEXT DEFAULT ('[]'),
  PRIMARY KEY (`identifier`),
  KEY `id` (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8mb4;
```

# License

    QBCore Framework
    Copyright (C) 2021 Joshua Eger

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>
