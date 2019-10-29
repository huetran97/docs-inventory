
#### List warehouse item
- Endpoint: `/inventory/warehouse_item_status/list`
- Method: `GET`
- Queries: 
    + `offset`: Number, Optional
    + `limit`: Number, Optional
- Response: `JSON`
    + `error_code`: Integer
    + `message`: String
    + `data`: Object
        + `total`: Number
        + `data`: Array Object
            + `id`: String
            + `name`: String
            + `color`: String

 
        