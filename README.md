# opsview-auth-template
Simple framework to interact with the Opsview rest API.
There is some regex logic to show out of balence VIPs you can add your own if you wish. Initialize the class:

	connection = OpsviewRest.new("http://opsviewservername.com", :username => "username", :password => "password")

Call the function with what ever host you want:

	json_file = connection.getServiceStatus("monitored.server.com")

You can just dump the json to stdout if you wish and stop there:
	
	pp connection.getServiceStatus("monitored.server.com")

