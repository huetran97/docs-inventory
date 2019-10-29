
#### List warehouse item
- Endpoint: `/inventory/tracking/list`
- Method: `GET`
- Queries: 
    + `offset`: Number, Optional
    + `limit`: Number, Optional
    + `sku`: String, Optional
    + `ref_type`: String {`ADD_WAREHOUSE_ITEM`, `MOVE_WAREHOUSE_ITEM`}
- Response: `JSON`
    + `error_code`: Integer
    + `message`: String
    + `data`: Object
        + `total`: Number
        + `data`: Array Object
            + `id`: String
            + `warehouse_item_id`: String
            + `description`: String
            + `ref_type`:  String {`ADD_WAREHOUSE_ITEM`, `MOVE_WAREHOUSE_ITEM`}
            + `timestamp`: Number

 
        