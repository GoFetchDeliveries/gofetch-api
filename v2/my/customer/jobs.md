# Customer Jobs

Manage a customer's jobs

* [Create a new customer job](#create-a-new-customer-job)

## Create a new customer job


### Request url
`POST`
`https://go-fetch.com.au/api/v1/my/customer/jobs.json`


### Headers

`X-User-Email: someemail@gmail.com`

`X-User-Token: TOKEN`

`Content-Type: application/json`

TOKEN is retrieved from the [User sign In](../../../v1/users/sign_in.md) endpoint

### Request body

```JSON
{
  "job": {
    "pickup_attributes": {
      "coordinates": {
        "lat": -37.8202508,
        "lon": 144.95645289999993
      },
      "address": "7 Katherine Pl, Melbourne VIC 3000, Australia",
      "suburb_name": "Melbourne",
      "postcode": "3000",
      "contact_id": "81c40ba2-5fca-4672-8dfe-0e1b796e56b8"
    },
    "dropoff_attributes": {
      "coordinates": {
        "lat": -37.815407,
        "lon": 144.95844290000002
      },
      "address": "520 Bourke St, Melbourne VIC 3004, Australia",
      "suburb_name": "Melbourne",
      "postcode": "3004",
      "contact_id": "81c40ba2-5fca-4672-8dfe-0e1b796e56b8"
    },
    "notes": "",
    "credit_card_id": "3811a73a-21bd-4eb9-af41-a224e0bbe6c7",
    "total_duration": 402,
    "total_distance": 788,
    "item_type_id": "9c509a8e-1309-4c03-ad1b-593eeb6d1048",
    "deliver_by": 1489533600000
  },
  "distance_based_pricing": true
}
```

### Response

```JSON
{
  "job": {
    "state": "pending",
    "id": "c46e3abe-6e31-4bf2-9de1-f8efee3b499e",
    "price_cents": 964,
    "notes": "",
    "created_at": "2017-03-31T11:36:26.003+11:00",
    "updated_at": "2017-03-31T11:36:26.003+11:00",
    "deliver_by": null,
    "conversation_id": null,
    "total_duration": 402,
    "total_distance": 788,
    "received_by": null,
    "signature_url": null,
    "delivered_at": null,
    "distance_travelled": null,
    "time_taken": null,
    "customer_id": "78fe11df-c550-4f85-a13d-ce15a5ce7f55",
    "customer_rated": null,
    "fetcher_rated": null,
    "payment_status": "pending",
    "picked_up_at": null,
    "promotional_code_used": false,
    "pickup_id": "5a18d660-e4f5-44a9-8d8f-d60e881439b7",
    "dropoff_id": "caa8d3ea-37a9-4ec1-9c99-79f0c0827764",
    "offer_ids": [],
    "item_type_id": "9c509a8e-1309-4c03-ad1b-593eeb6d1048",
    "credit_card_id": "3811a73a-21bd-4eb9-af41-a224e0bbe6c7"
  },
  "contacts": [
    {
      "id": "81c40ba2-5fca-4672-8dfe-0e1b796e56b8",
      "user_id": "9a3bc89e-731e-4af4-8f6c-79d1749c6557",
      "name": "Kyle",
      "phone": "12434567",
      "created_at": "2016-04-28T13:33:00.961+10:00",
      "updated_at": "2016-04-28T13:33:00.961+10:00",
      "profile_image_url": null,
      "from_address_book": false
    },
    {
      "id": "81c40ba2-5fca-4672-8dfe-0e1b796e56b8",
      "user_id": "9a3bc89e-731e-4af4-8f6c-79d1749c6557",
      "name": "Kyle",
      "phone": "12434567",
      "created_at": "2016-04-28T13:33:00.961+10:00",
      "updated_at": "2016-04-28T13:33:00.961+10:00",
      "profile_image_url": null,
      "from_address_book": false
    }
  ],
  "suburbs": [
    {
      "id": "1cdc7075-de9f-4e9d-ab92-8acbfe513934",
      "name": "MELBOURNE",
      "postcode": "3000",
      "display_name": "Melbourne, 3000"
    },
    {
      "id": "db107cb0-ece4-4660-98fd-444f0a998a86",
      "name": "SOUTHBANK",
      "postcode": "3006",
      "display_name": "Southbank, 3006"
    }
  ],
  "destinations": [
    {
      "id": "5a18d660-e4f5-44a9-8d8f-d60e881439b7",
      "job_id": "c46e3abe-6e31-4bf2-9de1-f8efee3b499e",
      "type": "Pickup",
      "created_at": "2017-03-31T11:36:26.097+11:00",
      "updated_at": "2017-03-31T11:36:26.097+11:00",
      "coordinates": {
        "lat": -37.8202508,
        "lon": 144.95645289999993
      },
      "address": "7 Katherine Pl, Melbourne VIC 3000, Australia",
      "suburb_name": "SOUTHBANK",
      "postcode": "3006",
      "contact_id": "81c40ba2-5fca-4672-8dfe-0e1b796e56b8",
      "suburb_id": "db107cb0-ece4-4660-98fd-444f0a998a86"
    },
    {
      "id": "caa8d3ea-37a9-4ec1-9c99-79f0c0827764",
      "job_id": "c46e3abe-6e31-4bf2-9de1-f8efee3b499e",
      "type": "Dropoff",
      "created_at": "2017-03-31T11:36:26.124+11:00",
      "updated_at": "2017-03-31T11:36:26.124+11:00",
      "coordinates": {
        "lat": -37.815407,
        "lon": 144.95844290000002
      },
      "address": "520 Bourke St, Melbourne VIC 3004, Australia",
      "suburb_name": "MELBOURNE",
      "postcode": "3000",
      "contact_id": "81c40ba2-5fca-4672-8dfe-0e1b796e56b8",
      "suburb_id": "1cdc7075-de9f-4e9d-ab92-8acbfe513934"
    }
  ],
  "offers": [],
  "item_types": [
    {
      "id": "9c509a8e-1309-4c03-ad1b-593eeb6d1048",
      "name": "Small food delivery",
      "created_at": "2016-08-02T11:43:07.059+10:00",
      "updated_at": "2016-09-27T17:07:48.964+10:00"
    }
  ],
  "credit_cards": [
    {
      "id": "3811a73a-21bd-4eb9-af41-a224e0bbe6c7",
      "stripe_card_id": "card_17yWKPHBLq9etHDK5BkxR5SL",
      "last_4_digits": "1512",
      "exp_month": "4",
      "exp_year": "2017",
      "brand": "Visa",
      "is_default": false,
      "customer_id": "78fe11df-c550-4f85-a13d-ce15a5ce7f55",
      "customer_type": "Customer",
      "created_at": "2016-04-10T10:21:29.699+10:00",
      "updated_at": "2016-04-10T10:21:29.699+10:00",
      "name": "MR DUY A DAO",
      "last_validated_at": "2016-04-10T10:21:29.696+10:00"
    }
  ],
  "meta": {
    "message": null
  }
}
```
