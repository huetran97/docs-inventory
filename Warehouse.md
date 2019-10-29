#### List warehouse
- Endpoint: `/inventory/warehouse/list`
- Method: `GET`
- Queries: 
    + `offset`: Number, Optional
    + `limit`: Number, Optional
    + `name`: String, Optional
- Response: `JSON`
    + `error_code`: Integer
    + `message`: String
    + `data`: Object
        + `total`: Number
        + `data`: Array Object
            + `id`: String
            + `name`:  String
            + `description`: String
            + `local_id`: String

#### Warehouse details
- Endpoint: `/inventory/warehouse/{warehouse_id}`
- Method: `GET`
- Response: `JSON`
    + `error_code`: Integer
    + `message`: String
    + `data`: Object
        + `id`: String
        + `name`:String
        + `descripton`: String
        + `local_id`: String
        