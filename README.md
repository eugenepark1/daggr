# daggr
data aggregator

These are 10 best practices to design a clean RESTful API:
	1. use nouns but no verbs
		resource	get (read)	post (create)	put (update)	delete 
		/cars		ret all cars	create a car	update cars	delete all cars
		/cars/711	ret spec car	NOT ALLOWED	update car	delete car
