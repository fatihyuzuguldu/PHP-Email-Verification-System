Make the Email stmp settings on line 146 in Login.php. <br>
Make the database settings in the Vt.php section. <br>

<br>

SQL Generation commands are given below.

<br><br><br>

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";
CREATE TABLE `users` (
	`id` VARCHAR(36) NOT NULL DEFAULT uuid() COLLATE 'utf8mb4_general_ci',
	`Email` VARCHAR(50) NOT NULL COLLATE 'utf8mb4_general_ci',
	`Name` VARCHAR(50) NOT NULL COLLATE 'utf8mb4_general_ci',
	`Username` VARCHAR(50) NOT NULL COLLATE 'utf8mb4_general_ci',
	`Password` VARCHAR(150) NOT NULL COLLATE 'utf8mb4_general_ci',
	`LastLogin` DATETIME NULL DEFAULT NULL,
	`2FA` INT(11) NULL DEFAULT '1',
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='utf8mb4_general_ci'
ENGINE=MyISAM
;
