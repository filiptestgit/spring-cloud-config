## Spring-cloud-config server

##### Dynamic routes refresh at config-client-side:
	1. change the desired configuration at server-side (eg. gateway-server-development.properties)
	2. git add .
	3. git commit -m "Properties change XYZ."
	4. git push
	5. curl -X POST localhost:_client_port_/actuator/refresh
	6. response should be an array of strings containing changed properties' name
