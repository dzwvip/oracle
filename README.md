# GORM Oracle Driver


## Description

GORM Oracle driver for connect Oracle DB and Manage Oracle DB, Based on [CengSin/oracle](https://github.com/CengSin/oracle)
，not recommended for use in a production environment
## DB Driver
[godror](https://github.com/godror/godror) 
## Required dependency Install

- Oracle 12C+
- Golang 1.13+
- see [ODPI-C Installation.](https://oracle.github.io/odpi/doc/installation.html)
- gorm 1.24.0+
- godror 0.33+
## Quick Start
### how to install 
```bash
go get github.com/dzwvip/oracle
```
###  usage

```go
import (
	"fmt"
	"github.com/dzwvip/oracle"
	"gorm.io/gorm"
	"log"
)

func main() {
    dsn := "oracle://system:manager@127.0.0.1:1521/db"
    db, err := gorm.Open(oracle.Open(dsn), &gorm.Config{})
    if err != nil {
        // panic error or log error info
    } 
    
    // do somethings
}
```
