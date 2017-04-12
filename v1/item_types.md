
Get all available item types.

* [Get Item Types](#get-item-types)

# Get Item Types

Retrieves all item types

### Request url

`GET`

http://test.go-fetch.com.au/api/v1/item_types.json

### Response

```JSON
{
  "item_types": [
    {
      "id": "3e39262b-b1d8-42d5-a781-444a08d479d4",
      "name": "Envelope/Document",
      "created_at": "2015-10-01T17:44:31.690+10:00",
      "updated_at": "2017-04-12T13:35:23.724+10:00",
      "fee_cents": 0
    },
    {
      "id": "6c990db6-a3d0-469f-b68e-a2086d0b9194",
      "name": "8 - 22kg",
      "created_at": "2015-10-15T11:21:09.294+11:00",
      "updated_at": "2017-01-31T19:58:48.778+11:00",
      "fee_cents": 0
    },
    {
      "id": "48e6747d-bd21-4494-aee1-8cfc2411aa5e",
      "name": "Up to 8kg (40cm x 40cm)",
      "created_at": "2015-10-01T17:44:31.686+10:00",
      "updated_at": "2015-10-01T17:44:31.686+10:00",
      "fee_cents": 0
    },
    {
      "id": "51f04d8f-128a-4a1f-87d8-33a12a932e32",
      "name": "I need a van/small truck (add $50)",
      "created_at": "2016-07-25T12:48:50.489+10:00",
      "updated_at": "2017-04-05T17:01:46.050+10:00",
      "fee_cents": 5000
    },
    {
      "id": "b1423f49-462e-4bc9-bd6e-4a5bb9385647",
      "name": "Small/Light floral arrangement",
      "created_at": "2016-09-24T12:43:58.738+10:00",
      "updated_at": "2017-01-10T12:27:12.577+11:00",
      "fee_cents": 0
    },
    {
      "id": "8904c2a1-80ed-40dc-8844-b9bbc8de4e65",
      "name": "Small gift",
      "created_at": "2015-12-09T12:57:34.653+11:00",
      "updated_at": "2016-09-27T17:07:59.174+10:00",
      "fee_cents": 0
    },
    {
      "id": "53b9c9a3-9ed1-4e51-aa3c-7444f73584a5",
      "name": "Fragile",
      "created_at": "2016-04-08T09:37:50.416+10:00",
      "updated_at": "2016-04-08T09:37:50.416+10:00",
      "fee_cents": 0
    },
    {
      "id": "5852b88c-9771-49b2-9aee-5325ed41bab8",
      "name": "Large/Fragile floral arrangement",
      "created_at": "2016-05-26T15:56:08.062+10:00",
      "updated_at": "2017-01-10T12:13:38.351+11:00",
      "fee_cents": 0
    },
    {
      "id": "9c509a8e-1309-4c03-ad1b-593eeb6d1048",
      "name": "Small food delivery",
      "created_at": "2016-08-02T11:43:07.059+10:00",
      "updated_at": "2016-09-27T17:07:48.964+10:00",
      "fee_cents": 0
    },
    {
      "id": "f1a47eff-640a-408b-9919-2a2de501c78a",
      "name": "Dry cleaning",
      "created_at": "2015-12-04T16:59:39.260+11:00",
      "updated_at": "2017-04-12T13:35:12.567+10:00",
      "fee_cents": 0
    }
  ],
  "meta": {
    "deleted_ids": [],
    "pagination": {
      "total_objects": 10
    }
  }
}
```
