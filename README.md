# Sqlite Storage for [OAuth 2.0](https://github.com/go-oauth2/oauth2)

[![Build][Build-Status-Image]][Build-Status-Url] [![Codecov][codecov-image]][codecov-url]  [![GoDoc][godoc-image]][godoc-url] [![License][license-image]][license-url]

## Install

```bash
$ go get -u -v github.com/bjaiwu/go-oauth2-sqlite
```


## Usage example

```go
package main

import (
    "database/sql"
	_ "github.com/mattn/go-sqlite3"
	sqlite "github.com/bjaiwu/go-oauth2-sqlite"
	"github.com/jmoiron/sqlx"
)

func main() {

	db, err = sql.Open("sqlite3", "file:db.db?cache=shared") //若数据库没有在这个项目文件下，则需要写绝对路径
	if err != nil {
		panic(err.Error())
	}

	clientStore, _ := sqlite.NewClientStore(db, mysql.WithClientStoreTableName("custom_table_name"))
	tokenStore, _ := sqlite.NewTokenStore(db)
}

```

## MIT License

```
Copyright (c) 2021 yxge.net
```

