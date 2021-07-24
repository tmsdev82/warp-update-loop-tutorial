# Rust Warp websocket server update loop tutorial

This repository to the article on my blog describing how to add a data update loop to a Warp WebSocket server with Rust. The data update loop continuously sends data to all the clients. The article can be found on my blog here: [TMS Blog - Rust Warp data update loop: easy how to](https://tms-dev-blog.com/rust-warp-data-update-loop-easy-how-to/)

WebSocket clients will be able to connect to 127.0.0.1:8000/ws, once connected the client will receive JSON data like the following, every 2 seconds:

```json
[
  {
    "creation_date" : "2021-07-24T06:50:27.374860Z",
    "widget_count" : 86,
    "widget_type" : "widget0"
  },
  {
    "creation_date" : "2021-07-24T06:50:27.374873Z",
    "widget_count" : 20,
    "widget_type" : "widget1"
  },
  {
    "creation_date" : "2021-07-24T06:50:27.374874Z",
    "widget_count" : 28,
    "widget_type" : "widget2"
  },
  {
    "creation_date" : "2021-07-24T06:50:27.374876Z",
    "widget_count" : 24,
    "widget_type" : "widget3"
  },
  {
    "creation_date" : "2021-07-24T06:50:27.374877Z",
    "widget_count" : 83,
    "widget_type" : "widget4"
  },
  {
    "creation_date" : "2021-07-24T06:50:27.374881Z",
    "widget_count" : 66,
    "widget_type" : "widget5"
  },
  {
    "creation_date" : "2021-07-24T06:50:27.374882Z",
    "widget_count" : 84,
    "widget_type" : "widget6"
  },
  {
    "creation_date" : "2021-07-24T06:50:27.374883Z",
    "widget_count" : 74,
    "widget_type" : "widget7"
  },
  {
    "creation_date" : "2021-07-24T06:50:27.374884Z",
    "widget_count" : 28,
    "widget_type" : "widget8"
  },
  {
    "creation_date" : "2021-07-24T06:50:27.374970Z",
    "widget_count" : 6,
    "widget_type" : "widget9"
  }
]
```

## Running the server

Simply use the use the `cargo run` command to run the program. There is no additional configuration needed.

The server will run on 127.0.0.1:8000.