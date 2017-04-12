
Calculate a potential job's price

* [Job Price Calculation](#job-price-calculation)

# Job Price Calculation

Calculates the job's price.

### Request url

`GET`

http://test.go-fetch.com.au/api/v2/jobs/calculate.json?distance_meters=802&item_weight=12&lat=-37.8278185&lon=144.9666907

### Query Parameters

##### distance_meters

A primary parameter used to calculate the delivery price.

##### lat

Latitude of the pickup address. Used as a backup in case suburb_name and postcode are not provided.

##### lon

Longitude of the pickup address. Used as a backup in case suburb_name and postcode are not provided.

##### suburb_name

Suburb name of the pickup address.

##### postcode

Suburb postcode of the pickup address.

##### item_weight

The weight of the item that needs to be delivered. Measured in kg.

##### item_type_id

The type of the item that needs to be delivered. This is an alternative to the item_weight parameter in case you definitely know the weight of the item.

### Response

```JSON
{
  "price_cents": 966
}
```
