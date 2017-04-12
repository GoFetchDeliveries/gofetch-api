
# Users

Manage your users.

* [Sign in](#sign-in)

## Sign In
### Request URL

`POST`
`https://go-fetch.com.au/api/v1/users.json`

Signs in using an email and a password and returns a user object with an authentication token that should be used in the X-User-Token header in future requests.

### Request data

```JSON
{
  "user": {
    "email": "someemail@gmail.com", 
    "password": "somepassword"
  }
}
```

### Response

Pay attention to the "authentication_token" in the response. This is what you will need to supply in future API requests.

```JSON
{
  "user": {
    "id": "9a3bc89e-731e-4af4-8f6c-79d1749c6557",
    "city": {
      "id": "b27e90a2-868d-48e7-aa43-3c35e7e481d4",
      "name": "Brisbane",
      "created_at": "2017-02-06T23:32:17.440+11:00",
      "updated_at": "2017-02-06T23:32:17.440+11:00",
      "coordinates": {
        "lat": -27.4750682,
        "lon": 153.0385987
      },
      "timezone": ""
    },
    "first_name": "John",
    "last_name": "Citizen",
    "email": "someemail@gmail.com",
    "profile_image_url": "https://somewhere/something.jpg",
    "phone": "0450651357",
    "is_business": false,
    "authentication_token": "A6xFwZV7TtUi3wNpTkEj",
    "customer_id": "78fe11df-c550-4f85-a13d-ce15a5ce7f55",
    "fetcher_id": "1f275943-3d70-459c-9c6f-78edee23f6b2",
    "self_contact_id": "24789b23-e139-43fa-97f1-043e702510ed",
    "referral_code": {
      "id": "655a3863-16cd-4ffe-aebb-0adab0d9c8c4",
      "code": "ANH0141",
      "referrer_id": "9a3bc89e-731e-4af4-8f6c-79d1749c6557",
      "owner_id": null,
      "updated_at": "2016-02-04T22:29:59.907+11:00",
      "amount_cents": 1000
    }
  },
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
  "contacts": [
    {
      "id": "4cedf31b-5bfd-4b96-bb3f-c63e798c3193",
      "user_id": "9a3bc89e-731e-4af4-8f6c-79d1749c6557",
      "name": "JP Iturrieta",
      "phone": "450235510",
      "created_at": "2017-02-21T14:17:14.874+11:00",
      "updated_at": "2017-02-21T14:17:14.874+11:00",
      "profile_image_url": null,
      "from_address_book": false
    },
    {
      "id": "24789b23-e139-43fa-97f1-043e702510ed",
      "user_id": "9a3bc89e-731e-4af4-8f6c-79d1749c6557",
      "name": "John Citizen",
      "phone": "0422281607",
      "created_at": "2016-02-04T22:29:59.855+11:00",
      "updated_at": "2017-03-19T19:01:40.292+11:00",
      "profile_image_url": "https://somewhere/image.jpg",
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
      "id": "50ace2e1-0f78-450d-87ab-cf00c9a92b4c",
      "name": "SOUTH YARRA",
      "postcode": "3141",
      "display_name": "South Yarra, 3141"
    }
  ],
  "recent_destinations": [
    {
      "id": "3fec88af-ff84-4c36-8599-49c9616e81f1",
      "job_id": "7ecc6cd3-16c5-4cae-9cb4-c4cdb1a39da1",
      "type": "Dropoff",
      "created_at": "2017-03-30T13:34:57.256+11:00",
      "updated_at": "2017-03-30T13:34:57.256+11:00",
      "coordinates": {
        "lat": -37.8152745,
        "lon": 144.95837340000003
      },
      "address": "520 Bourke St, Melbourne VIC 3004, Australia",
      "suburb_name": "MELBOURNE",
      "postcode": "3000",
      "contact_id": "4cedf31b-5bfd-4b96-bb3f-c63e798c3193",
      "suburb_id": "1cdc7075-de9f-4e9d-ab92-8acbfe513934"
    },
    {
      "id": "d147a38c-ad6a-4f6c-81b5-73539da3f86b",
      "job_id": "e6939b2a-1d48-4ccb-8acf-423e5f25a3f7",
      "type": "Pickup",
      "created_at": "2017-03-22T10:13:18.595+11:00",
      "updated_at": "2017-03-22T10:13:18.595+11:00",
      "coordinates": {
        "lat": -37.8130568,
        "lon": 144.9735601
      },
      "address": "710/2 Collins St, Melbourne VIC 3000, Australia",
      "suburb_name": "MELBOURNE",
      "postcode": "3000",
      "contact_id": "24789b23-e139-43fa-97f1-043e702510ed",
      "suburb_id": "1cdc7075-de9f-4e9d-ab92-8acbfe513934"
    },
    {
      "id": "9fcc547e-fb00-40ee-924e-7ac6b57031e6",
      "job_id": "6fbec3dc-c338-4f74-94aa-c00056d64da8",
      "type": "Pickup",
      "created_at": "2017-03-22T10:06:34.493+11:00",
      "updated_at": "2017-03-22T10:06:34.493+11:00",
      "coordinates": {
        "lat": -37.83751639999999,
        "lon": 144.99306690000003
      },
      "address": "9 Yarra St, South Yarra VIC 3141, Australia",
      "suburb_name": "SOUTH YARRA",
      "postcode": "3141",
      "contact_id": "24789b23-e139-43fa-97f1-043e702510ed",
      "suburb_id": "50ace2e1-0f78-450d-87ab-cf00c9a92b4c"
    },
    {
      "id": "ff8a47c6-d3c5-4d0c-83b7-149802e1ebbe",
      "job_id": "1598ff19-5ba7-4afb-aa48-61650fc1d1c2",
      "type": "Dropoff",
      "created_at": "2017-03-21T16:22:44.882+11:00",
      "updated_at": "2017-03-21T16:22:44.882+11:00",
      "coordinates": {
        "lat": -37.8087172533393,
        "lon": 144.9684207513928
      },
      "address": "8 Exploration Lane, Melbourne",
      "suburb_name": "MELBOURNE",
      "postcode": "3000",
      "contact_id": "24789b23-e139-43fa-97f1-043e702510ed",
      "suburb_id": "1cdc7075-de9f-4e9d-ab92-8acbfe513934"
    },
    {
      "id": "3f7076ee-8fe2-482b-87c8-9dad850d239f",
      "job_id": "1598ff19-5ba7-4afb-aa48-61650fc1d1c2",
      "type": "Pickup",
      "created_at": "2017-03-21T16:22:44.878+11:00",
      "updated_at": "2017-03-21T16:22:44.878+11:00",
      "coordinates": {
        "lat": -37.82410595617564,
        "lon": 144.9647803232074
      },
      "address": "57-83 Kavanagh Street, Southbank",
      "suburb_name": "MELBOURNE",
      "postcode": "3000",
      "contact_id": "24789b23-e139-43fa-97f1-043e702510ed",
      "suburb_id": "1cdc7075-de9f-4e9d-ab92-8acbfe513934"
    }
  ],
  "customers": [
    {
      "id": "78fe11df-c550-4f85-a13d-ce15a5ce7f55",
      "first_name": "John",
      "last_name": "Citizen",
      "profile_image_url": "https://somewhere/something.jpg",
      "updated_at": "2017-03-31T11:02:33.697+11:00",
      "phone": "0450651357",
      "average_rating": 5,
      "user_id": "9a3bc89e-731e-4af4-8f6c-79d1749c6557",
      "credit_card_ids": [
        "3811a73a-21bd-4eb9-af41-a224e0bbe6c7"
      ],
      "recent_destination_ids": [
        "3fec88af-ff84-4c36-8599-49c9616e81f1",
        "d147a38c-ad6a-4f6c-81b5-73539da3f86b",
        "9fcc547e-fb00-40ee-924e-7ac6b57031e6",
        "ff8a47c6-d3c5-4d0c-83b7-149802e1ebbe",
        "3f7076ee-8fe2-482b-87c8-9dad850d239f"
      ]
    }
  ],
  "transport_types": [
    {
      "id": "568c4ee4-cf80-4eb7-8bdf-c5fffdd7514d",
      "name": "Walking",
      "is_visible": true,
      "created_at": "2015-10-01T17:44:31.701+10:00",
      "updated_at": "2017-02-09T13:48:59.846+11:00",
      "svg_path": "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<svg width=\"19px\" height=\"27px\" viewBox=\"0 0 19 27\" version=\"1.1\" xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\">\n    <!-- Generator: Sketch 41.2 (35397) - http://www.bohemiancoding.com/sketch -->\n    <title>walking</title>\n    <desc>Created with Sketch.</desc>\n    <defs></defs>\n    <g id=\"Page-1\" stroke=\"none\" stroke-width=\"1\" fill=\"none\" fill-rule=\"evenodd\">\n        <g id=\"walking\" transform=\"translate(1.000000, 1.000000)\" stroke-width=\"0.5\" stroke=\"#000000\" fill=\"#000000\">\n            <g id=\"Fetcher---Dashboard-+-Jobs\">\n                <g id=\"3.0---Dashboard---Change-Transport-type\">\n                    <g id=\"Top-and-Hold-Menu\" transform=\"translate(0.500000, 0.000000)\">\n                        <g id=\"transport_type_walking\" transform=\"translate(0.274879, 0.824008)\">\n                            <path d=\"M10.6315646,2.9684263 C10.6315646,4.1244926 9.6947445,5.0617592 8.5386782,5.0617592 C7.3826119,5.0617592 6.4453453,4.1244926 6.4453453,2.9684263 C6.4453453,1.81235995 7.3826119,0.87553989 8.5386782,0.87553989 C9.6947445,0.87553989 10.6315646,1.81235995 10.6315646,2.9684263 L10.6315646,2.9684263 Z M9.1075575,7.3573702 C8.929392,6.6755188 8.2805838,5.9918813 7.5960533,5.9918813 L6.5435819,5.9918813 C5.9903312,5.9918813 5.7880531,6.1941594 5.4504763,6.3825951 L2.6020611,8.803681 C2.3493251,8.9483568 2.1908069,9.1613516 2.0930168,9.4654386 L1.3598145,13.3502501 C1.2722946,14.0035236 1.6161227,14.2799257 2.0072831,14.3607476 C2.3243194,14.425941 2.8034462,14.2660832 2.8981105,13.8079434 C2.9758068,13.430179 3.6750728,10.2928588 3.6750728,10.2928588 L5.5348705,8.8675348 C5.2289974,10.2883935 4.9173195,11.848123 4.8137245,12.375475 C4.6364521,13.2814845 5.0896801,13.9704803 5.4446715,14.5058699 C5.7701919,14.9970529 9.9778446,21.6190937 10.5328815,22.3397932 C11.0879183,23.0600462 11.5924973,23.4168237 12.36812,22.9863687 C13.0155886,22.626912 12.9079748,21.8008314 12.5480716,21.1899783 C12.1881684,20.5791252 7.9425606,13.6806823 7.9425606,13.6806823 C7.9425606,13.6806823 8.9811895,9.041235 9.0745143,8.6143523 C9.1678391,8.187023 9.2464284,7.888741 9.1075575,7.3573702 L9.1075575,7.3573702 Z M4.8320322,13.3466778 L3.5527236,17.99193 C3.5527236,17.99193 1.7590124,20.5849301 1.2597918,21.3109879 C0.8855996,21.8557546 0.6038391,22.5210844 1.2455028,23.005123 C1.9648627,23.547657 2.54044,22.8403534 2.9137391,22.4210617 C3.2557811,22.0370458 4.6440431,20.0973192 5.0378826,19.6025639 C5.2999957,19.2734713 5.4446715,18.9948365 5.5558574,18.7175414 C5.6299814,18.5326779 6.5181297,16.2102751 6.5181297,16.2102751 L4.8320322,13.3466778 Z M8.6565622,10.6090021 C8.6565622,10.6090021 9.1495313,11.3091612 9.4040535,11.7047868 C9.5255096,11.8932225 9.6514311,11.9655604 9.984096,12.1490842 C10.3757029,12.3647582 12.2841723,12.9849885 12.8615357,13.2426363 C13.3737057,13.4712597 14.0109041,13.5592261 14.2676588,13.1059981 C14.5244136,12.6527701 14.1971071,12.1124688 13.8135378,11.9369825 C13.3946926,11.7449745 10.6056659,10.6076625 10.6056659,10.6076625 C10.6056659,10.6076625 9.582219,8.4107346 9.0736212,7.2609197 L8.6565622,10.6090021 Z\" id=\"icon_walk-copy\"></path>\n                        </g>\n                    </g>\n                </g>\n            </g>\n        </g>\n    </g>\n</svg>"
    }
  ],
  "fetchers": [
    {
      "id": "1f275943-3d70-459c-9c6f-78edee23f6b2",
      "first_name": "John",
      "last_name": "Citizen",
      "profile_image_url": "https://somewhere/something.jpg",
      "is_approved": true,
      "state": "inactive",
      "updated_at": "2017-03-31T11:02:33.701+11:00",
      "average_rating": 5,
      "phone": "0450651357",
      "requires_confirmation": true,
      "requires_stripe_setup": true,
      "user_id": "9a3bc89e-731e-4af4-8f6c-79d1749c6557",
      "transport_type_id": "568c4ee4-cf80-4eb7-8bdf-c5fffdd7514d"
    }
  ]
}
```
