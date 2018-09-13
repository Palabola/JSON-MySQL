# JSON-MySQL

- Small module to generate MySQL Table from any given JSON.


# How to use

const json_mysql = require("json-mysql");

let test_json = JSON.parse('{"name": "John Snow", "age": 35}');

let table_name = 'Actors';

let table = new json_mysql(table_name,test_json);


console.log(table.query);

/*
CREATE TABLE IF NOT EXISTS `Actors` (
`name` VARCHAR (255)  NOT NULL,
`age` INT (10)  NOT NULL DEFAULT '0'
) ENGINE=INNODB DEFAULT CHARSET=utf8;
*/