
Calculate a potential job's price

* [Job Price Calculation](#job-price-calculation)

# Job Price Calculation

Calculates the job's price based on distance or (deprecated) seconds parameter.

### Request url

`GET`

https://go-fetch.com.au/api/v1/jobs/calculate.json?distance_meters=802&seconds=403

### Query Parameters

##### distance_meters

A primary parameter used to calculate the delivery price.

##### seconds (Deprecated)
*Deprecated. Do not use it.*

If distance_meters is not provided, the job will be calculated based on the amount of time it will take to deliver it.

### Response

```JSON
{
  "price_cents": 966
}
```
