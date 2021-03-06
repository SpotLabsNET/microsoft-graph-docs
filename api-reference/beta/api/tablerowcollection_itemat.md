# TableRowCollection: ItemAt

Gets a row based on its position in the collection.
## Prerequisites
The following **scopes** are required to execute this API: 
## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables(<id|name>)/rows/ItemAt(index=n)
GET /workbook/worksheets(<id|name>)/tables(<id|name>)/rows/ItemAt(index=n)

```
## Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer <code>|


## Request body
In the request body, provide a JSON object with the following parameters.

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|index|number|Index value of the object to be retrieved. Zero-indexed.|

## Response
If successful, this method returns `200, OK` response code and [TableRow](../resources/tablerow.md) object in the response body.

## Example
Here is an example of how to call this API.
##### Request
Here is an example of the request. Returns 1st row. 
<!-- {
  "blockType": "request",
  "name": "tablerowcollection_itemat"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/<id>/workbook/tables(<id|name>)/rows/ItemAt(0)
```

##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableRow"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableRowCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
