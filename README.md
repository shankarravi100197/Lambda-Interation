# Lambda-Interation

Create a function

![Screenshot 2023-07-02 130735](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/39bb8076-42e6-4c41-96ac-89a1f920e937)

![Screenshot 2023-07-02 131115](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/eae625cd-2ab5-4106-b231-9a05cf950493)

Sample API
![Screenshot 2023-07-02 135450](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/25aded43-9568-4bf6-b407-de7f21afb74b)


Create config.py
   base_url = "https://jsonplaceholder.typicode.com"
   
   ![Screenshot 2023-07-02 135927](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/81806b8c-448a-4b9b-8601-732bf026e972)

   

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

![Screenshot 2023-07-02 140854](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/aa478f9e-492d-489a-bf9c-0f01e6acd0fa)

Here comes Layer, a layer will be created on function which cointain all requirement so your function has no problem


Create a Layer

Make a zip file to upload to Layer

mkdir pypackages

pip3 install requests -t (put the path of file or folder) example below-
pip3 install requests -t C:\Users\LENOVO\Downloads\pypackages

zip the pypackages (in windows you can click right button and make a zip file)

Upload the zip file in LAMBDA Layers
![Screenshot 2023-07-02 142536](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/aa6f570b-a266-43ca-8ee5-29745a7f3d96)


Then go to Functions learning-lambda and add a Layer
![Screenshot 2023-07-02 142838](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/0c53ac1a-9333-44f5-a965-8c78ccaafb75)


Go to API

Make REST API and New API
![Screenshot 2023-07-02 143314](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/b5e04c17-c740-4618-8706-5c7e7ffec36a)

create API

Go to Actions 
Create a Methods
Select GET Method
GET API
Enable CORS
Deploy API
![Screenshot 2023-07-02 143816](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/ada9aa94-22ed-44b1-b879-f0e3e73b34f7)


You will get URL and test it in POSTMAN

![Screenshot 2023-07-02 144149](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/1d156888-9b04-4cd2-9bd6-7d703c4ed81e)

Go to Learning-lambda
Add trigger
API Gateway
Add it
![Screenshot 2023-07-02 144544](https://github.com/shankarravi100197/Lambda-Interation/assets/109327386/c72d6f7b-934c-4e9a-92f2-b93217086771)


Now test the URL at any browser you will get the same result

We made API that too serverless








 
