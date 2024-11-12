# Json-RAML
Json : 
{

    "status": "Success",
    "message": {
        "correlationId": "d59b0f04-5783-470b-8699-f713686bb204",
        "data": [
            {
            "success":true,
                "deliveryType": "REG",
                "inactiveReason": "GEO_LMT",
                "activeIndicator": "N",
                "deliveryDate":null
            },
            {
                "success":true,
                "deliveryType": "EXP",
                "inactiveReason": "GEO_LMT",
                "activeIndicator": "N",
                "deliveryDate":null
            }
        ]
    }
}


RAML : 
#%RAML 1.0 DataType 
type: object
properties:
  status:
    type: string
    example: Success
  message:
    type: object
    properties:
      correlationId:
        type: string
        example: d59b0f04-5783-470b-8699-f713686bb204
      data:
        type: array
        items:
          type: object
          properties:
            success:
              type: boolean
              example: true
            deliveryType:
              type: string
              example: REG
            inactiveReason:
              type: string
              example: GEO_LMT
            activeIndicator:
              type: string
              example: 'N'
            deliveryDate:
              type: 'null'
              example: null
