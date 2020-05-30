# ByteBank

<p align="center">
  <img src="http://upload-gifs.s3-sa-east-1.amazonaws.com/b00af167-4d08-4a53-9db0-63a1cbeaea59_Screenshot_1590862221.png" width="200">
  <img src="http://upload-gifs.s3-sa-east-1.amazonaws.com/862f686c-9f03-476e-85a1-168e2fa68f6f_Screenshot_1590862299.png" width="200">
  <img src="http://upload-gifs.s3-sa-east-1.amazonaws.com/b0269d28-d9aa-4e10-83c6-f140554dfc97_Screenshot_1590862352.png" width="200">
  <img src="http://upload-gifs.s3-sa-east-1.amazonaws.com/55986e85-6ea4-468d-9e05-d433dec4e245_Screenshot_1590862647.png" width="200">
</p>

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

<br>

## Web API [required]
Spring Boot Web API for consumption of the ByteBank Flutter App

### Features
- `GET` show transactions
- `POST` create transaction

### How to run
```bash
$ java -jar server.jar
```
> the api was built based on Java 8, to work as expected, version 8 is recommended

### End-points
- GET: `/transactions`
```json
// demo response
[
    {
        "id": "b9663ef3-3749-400e-be8f-1280db94aac8",
        "value": 200.00,
        "contact": {
            "name": "Fulano",
            "accountNumber": 1000
        },
        "dateTime": "2020-05-30 15:32:13"
    },
    {
        "id": "d1bf689c-caa2-4e45-b1fc-5a90b10d6d48",
        "value": 200.00,
        "contact": {
            "name": "Beltrano",
            "accountNumber": 1500
        },
        "dateTime": "2020-05-30 15:36:23"
    }
]
```

- POST: `/transactions`
> It's necessary to send `password` = `1000` in the request header
```json
// demo request body
{
  	"value": 200.0,
  	"contact": {
  		"name": "Thompson",
  		"accountNumber": 1000
  	}
}

// demo response
{
      "id": "b9663ef3-3749-400e-be8f-1280db94aac8",
      "value": 200.00,
      "contact": {
          "name": "Thompson",
          "accountNumber": 1000
      },
      "dateTime": "2020-05-30 11:07:26"
}
```
