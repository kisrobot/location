# Location

Location picks up location details from an interactive Google Map widget when creating/editing any applicable Resource in [Qor Admin](http://github.com/kisrobot/admin).

# Usage

To use Location with [QOR Admin](http://github.com/kisrobot/admin), simply embed `location.Location` in a model then behold the map picker in the [QOR Admin](http://github.com/kisrobot/admin) interface.

```go
import (
  "github.com/jinzhu/gorm"
  "github.com/kisrobot/location"
)

type Store struct {
  gorm.Model
  Name string
  location.Location
}
```

Embedded `location.Location` brings these attributes to your struct

```go
type Location struct {
  Address   string
  City      string
  Region    string
  Country   string
  Zip       string
  Latitude  float64
  Longitude float64
}
```

Now, you can call `Store.Address` or `Store.Country` etc. to get the address of the store.

[Location Demo: http://demo.getqor.com/admin/setting](http://demo.getqor.com/admin/setting)

# License

Released under the [MIT License](https://github.com/jinzhu/gorm/blob/master/License).
