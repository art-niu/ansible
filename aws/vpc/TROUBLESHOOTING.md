Error:
    "msg": "Couldn't create route: An error occurred (InvalidParameterValue) when calling the CreateRoute operation: Route target is not supported. This route only supports interface and instance targets.",
    "response_metadata": {
        "http_headers": {
            "connection": "close",
            "date": "Mon, 22 Jun 2020 03:38:43 GMT",
            "server": "AmazonEC2",
            "transfer-encoding": "chunked"
        },
        "http_status_code": 400,
        "request_id": "c975a148-3f72-473f-b7dd-9ebea98a5641",
        "retry_attempts": 0
    }

Cause: 
    routes:
      - dest: "{{ private_route_table.dest }}"
        gateway_id: "{{ igw.gateway_id }}"

if gateway_id is using igw, dest must be 0.0.0.0/0


