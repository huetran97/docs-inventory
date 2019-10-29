#### Create new warehouse item
- Endpoint: `/inventory/warehouse_item`
- Method: `POST`
- Params: 
    + `item_id`: String, Required
    + `warehouse_id`: String, Required
    + `quantity`: Number, Required,
    + `sku`: String, Required
    + `status_id`: String, Optional
- Response: `JSON`
    + `error_code`: Integer
    + `message`: String
    + `data`: Object
        + `id`: String
        + `warehouse_id`: String
        + `item_id`: String
        + `quantity`: Number
        + `status_id`: String
        + `created_timestamp`: Number
        + `sku`: String

#### Move warehouse item
- Endpoint: `/inventory/warehouse_item`
- Method: `PATCH`
- Params: 
    + `new_warehouse_id`: String, Required
    + `id`: String, Required
- Response: `JSON`
    + `error_code`: Integer
    + `message`: String
    + `data`: Object
        + `id`: String
        + `warehouse_id`: String
        + `item_id`: String
        + `quantity`: Number
        + `status_id`: String
        + `created_timestamp`: Number
        + `sku`: String


#### List warehouse item
- Endpoint: `/inventory/warehouse_item/list`
- Method: `GET`
- Queries: 
    + `offset`: Number, Optional
    + `limit`: Number, Optional
    + `warehouse_id`: String, Required,
    + `sku`: String, Optional
    + `status_id`: String, Optional
- Response: `JSON`
    + `error_code`: Integer
    + `message`: String
    + `data`: Object
        + `total`: Number
        + `data`: Array Object
            + `id`: String
            + `item`: Object
                + `id`: String
                + `name`:  String
                + `unit`: Object
                    + `id`: String
                    + `name`: String
                + `description`: String
                + `local_id`: String
            + `quantity`: Number
            + `sku`: String
            + `status`: Object
                + `id`: String
                + `name`: String
                + `color`: String

        

#### Warehouse item details
- Endpoint: `/inventory/warehouse_item/{warehouse_item_id}`
- Method: `GET`
- Response: `JSON`
    + `error_code`: Integer
    + `message`: String
    + `data`: Array Object
        + `id`: String
        + `item`: Object
            + `id`: String
            + `name`:  String
            + `unit`: Object
                + `id`: String
                + `name`: String
            + `description`: String
            + `local_id`: String
        + `quantity`: Number
        + `sku`: String
        + `status`: Object
            + `id`: String
            + `name`: String
            + `color`: String

        