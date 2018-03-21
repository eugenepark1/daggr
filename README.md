# daggr
data aggregator

example HTTP endpoints, apache mesos operator HTTP API endpoint
	* http://mesos.apache.org/documentation/latest/operator-http-api/
	* Both masters and agents provide the /api/v1 endpoint as the base URL for operations
	* the operator endpoint only accept HTTP POST requests
	* The request body should be encoded in:
		* JSON (Content-Type: application/json) or 
		* Protobuf (Content-Type: application/x-protobuf)
	* For requests that Mesos can answer synchronosly and immediatly, an HTTP response 200 OK
	* For requests which require asnyc processing, an HTTP response 202 Accepted
	* For requests result in a stream/events, a streaming HTTP response with RecordIO encoding


These are 10 best practices to design a clean RESTful API:
	1. use nouns but no verbs
		resource	GET (read)	POST (create)	PUT (update)	DELETE 
		/cars		ret all cars	create a car	update cars	delete all cars
		/cars/711	ret spec car	NOT ALLOWED	update car	delete car
