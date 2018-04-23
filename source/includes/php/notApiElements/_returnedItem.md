### ReturnedItem

> Get a ReturnedItem

```php
<?php
require 'path/to/lib/shoprunback-php/init.php';

$shipback = \Shoprunback\Elements\Shipback::retrieve('1f27f9d9-3b5c-4152-98b7-760f56967dea');

$returnedItem = $shipback->returned_items[0];
```

The class ReturnedItem represents an item a customer ordered and wants to return.

A **Shipback owns an array of ReturnedItems**.

A **ReturnedItems** is **linked to an Item coming from the Order linked to the Shipback**.

#### Parameters

Parameter | Type | Description
-|-|-
**item_id** | **String** | The id of the linked Item
**reason_code** | **Enum: doesnt_fit, quality, damaged, wrong, incorrect, delay, reconsider** | The reason why the item is returned ordered