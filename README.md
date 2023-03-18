# GORM PostgreSQL Driver

## Quick Start

```go
import (
  "github.com/andreidm777/driver/postgres"
  "github.com/andreidm777/gorm"
)

// https://github.com/jackc/pgx
dsn := "host=localhost user=gorm password=gorm dbname=gorm port=9920 sslmode=disable TimeZone=Asia/Shanghai"
db, err := gorm.Open(postgres.Open(dsn), &gorm.Config{})
```

## Configuration

```go
import (
  "github.com/andreidm777/driver/postgres"
  "github.com/andreidm777/gorm"
)

db, err := gorm.Open(postgres.New(postgres.Config{
  DSN: "host=localhost user=gorm password=gorm dbname=gorm port=9920 sslmode=disable TimeZone=Asia/Shanghai", // data source name, refer https://github.com/jackc/pgx
  PreferSimpleProtocol: true, // disables implicit prepared statement usage. By default pgx automatically uses the extended protocol
}), &gorm.Config{})
```


Checkout [https://github.com/andreidm777](https://github.com/andreidm777) for details.
