# ZIP_arrays_together_vica_versa

Read attentively,   must select master branch

1. download jar file as zip

2. and import that jar file into anypointstudio(latest version)

3. open postman or visual studio plugin thunder client

4. copy this url "localhos:8081/dataweave/payload1 (or) payload2" (note:only pass one "uriparameter" as "payload1" or "payload2"
	
	ex:localhost:8081/payload1

5. and insert payloads in the body section of the "postman" or "thunderclient"

6. make sure when you pass payload1 as endpoint  insert bleow payload1 json data into the body part

listener configurations set to hard coded

path = /dataweave{payloadtype}
port = 8081
host = localhsot
protocol = http

payload1 = [
  {
    "name": "wooden-chair",
    "id": "23665",
    "screws": [[
        4,
        15
      ],
      [
        6,
        8
      ],
      [
        10,
        28
      ]],
    "measurements": [
      [
        25,
        15
      ],
      [
        46,
        4
      ],
      [
        46,
        4
      ],
      [
        16,
        80
      ],
      [
        150,
        3
      ],
      [
        5,
        4
      ],
      [
        100,
        4
      ],
      [
        100,
        15
      ]
    ]
  },
  {
    "name": "coffee-table",
    "id": "14398",
    "screws": [
      [
        3,
        8
      ],
      [
        8,
        12
      ],
      [
        10,
        20
      ]
    ],
    "measurements": [
      [
        55,
        55
      ],
      [
        48,
        40
      ],
      [
        48,
        40
      ],
      [
        48,
        40
      ],
      [
        48,
        50
      ],
      [
        30,
        4
      ],
      [
        30,
        4
      ],
      [
        30,
        4
      ],
      [
        30,
        4
      ]
    ]
  }
]


payload2 = [
   {
    "name":"wooden-chair",
    "itemID": "23665",
    "screws":{
      "size":[4,6,10],
      "quantity":[15,8,28]
    },
    "measurements":
    {"x":[25,46, 46, 16,150,5, 100, 100, 8],
    "y":[15,4, 4, 80,3, 4, 4, 15]
    }
  },
   {
    "name":"coffee-table",
    "itemID": "14398",
    "screws":{
      "size":[3,8,10],
      "quantity":[8,12,20]
    },
    "measurements":
    {"x":[55, 48, 48, 48, 48, 30, 30, 30, 30],
    "y":[55, 40, 40, 40, 50, 4, 4, 4, 4]
    }
  }
]
