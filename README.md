# Vaccine finder for India

## Features

- Check availability of vaccine by providing district code of your area
- Run in the terminal and monitor the vaccine availability
- It will show notification immediately when there is vaccines available.
- set age range to check availability in that range.


## Set Up

Vaccine-spotter requires [python3](https://www.python.org/downloads/) to run

Project dependencies can be installed using the following command:

``` sh
pip install -r requirements.txt
```


You can see vaccine availability using district code
``` sh 
area_info:
# [edit] enter your district code or pincode
  __district_code : "<district_code>" 
```

Run  
```sh
python3 vaccineSpotter.py

```
Then it'll search for vaccine availability in your area.


### Using district code
Set district code in the [config file](config.yml) file.
To know your district code follow these steps:

- First see your state code [here](https://cdn-api.co-vin.in/api/v2/admin/location/states) 

- Now edit your state code in this url https://cdn-api.co-vin.in/api/v2/admin/location/districts/{your_state_code} 
  e.g. https://cdn-api.co-vin.in/api/v2/admin/location/districts/16 for karnataka

- click on the url for your state you can see your district code by searching your district name.

Enter the district code in [config file](config.yml) file

Enter the center id according to your nearest center: 	
            "if (res['age_limit'] in self.age_limit): #and (res['center_id'] in self.centre_id_value)"
  Remove the '#' in the above statment in line no : 47 in vaccine.py
  update center id in config.yml , Find center id using district id and date
  https://cdn-api.co-vin.in/api/v2/appointment/sessions/public/calendarByDistrict?district_id=204&date=16-05-2021
  
``` sh 

area_info:
# [edit] enter your district code or pincode
  __district_code : "<district_code>"
```
Run the script after setting the values 
```sh
python3 vaccineSpotter.py

```
It'll search for availibility of vaccine centers in that area.


## Development

Want to contribute? Great! 
Feel free to raise a pull request :hugs:

