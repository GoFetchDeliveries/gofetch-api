
Calculate a potential job's price

* [Job Price Calculation](#job-price-calculation)

# Job Price Calculation

Calculates the job's price.

### Request url

`GET`

https://go-fetch.com.au/api/v2/jobs/calculate.json?distance_meters=802&item_type_id=6c990db6-a3d0-469f-b68e-a2086d0b9194&lat=-37.8278185&lon=144.9666907

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

##### item_type_id

The type of the item that needs to be delivered.

### Response

```JSON
{
  "price_cents": 966
}
```
