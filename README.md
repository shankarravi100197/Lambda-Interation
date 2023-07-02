# Lambda-Interation

Create a function

Create config.py
   base_url = "https://jsonplaceholder.typicode.com"

Create lambda_function.py
    import json
    from config import base_url
    import requests

    def lambda_handler(event, context):
    
         res = requests.get(url=base_url+'todos/1')
         return {
               'statusCode': res.status_code,
                'body': res.json()
          }

Deploy it

Create a Layer

mkdir pypackages

pip3 install requests -t C:\Users\LENOVO\Downloads\pypackages

zip the pypackages (using API)

Upload the zip file in LAMBDA Layers

Then go to Functions learning-lambda and add a Layer

Go to API

Make REST API and New API

create API

Go to Actions 

Create a Methods

GET API
Enable CORS
Deploy API

You will get URL and test it in POSTMAN

Go to learning-lambda
Add trigger
API Gateway
Add it

Now test the URL at any browser you will get the same result

We made API that too serverless








 
