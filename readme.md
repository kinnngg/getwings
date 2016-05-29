# GetWings Internship Test Project

This Project is developed using Laravel framework.
Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable, creative experience to be truly fulfilling. Laravel attempts to take the pain out of development by easing common tasks used in the majority of web projects, such as authentication, routing, sessions, queueing, and caching.

In this project User will be able to
1) Signup
2) Login/Login with Google
3) Get a token for API request.
4) Set and Change his location

Using API request a User can:
1) View his profile
2) View list of users who are online and resides very near to him with help of google maps api.

Finding of users distance in done thru distance formula and uses google maps api to get location and lng and lat.

## Request and Response Wiki

### Sample Nearby User Request
*Request*
``
http://getwings.app/api/v1/nearby?api_token=ImEUUzDTiWs3cRgVSGSy5fwhBPyR9YdjdyS3nAoWU2N4qw2txlTZiumtCdME
``
*Response*
```
[
  {
    "id": 2,
    "full_name": "Faiyaz Faizan",
    "address": "Mesra, Jharkhand, India",
    "distance": 2.94935297966003,
    "units": "kilometers",
    "is_online": true
  },
  {
    "id": 1,
    "full_name": "Zishan Ansari",
    "address": "Jamshedpur, Jharkhand 831001, India",
    "distance": 106.45262475559,
    "units": "kilometers",
    "is_online": false
  }
]
```

### Sample Profile Request
*Request*
``
http://getwings.app/api/v1/me?api_token=ImEUUzDTiWs3cRgVSGSy5fwhBPyR9YdjdyS3nAoWU2N4qw2txlTZiumtCdME
``

*Response*
```
{
  "full_name": "Faiyaz Faizan",
  "email": "faiyaz@test.com",
  "address": "Mesra, Jharkhand, India",
  "joined_on": {
    "date": "2016-05-29 10:53:55",
    "timezone_type": 3,
    "timezone": "UTC"
  }
}
```


## License

No License in assigned to this project right now.
