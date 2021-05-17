# webdns

		Pull the docker image:
		docker pull maxmengdocker/webdns:0.1
		
		Clone the base:
		git clone https://github.com/maxmengtor/webdns.git
		
		Start the container:
		docker run -p 53:53/udp -p 53:53/tcp -p 8180:8180/tcp -v /sys/fs/cgroup:/sys/fs/cgroup:ro --privileged -v ./webdns:/webdns --user root -dit webdns:0.2
		Start the services:
		docker exec {CONTAINER} /entrypoint.sh
		
		Set it up with http://127.0.0.1:8180/namedmanager
		User/Pass as setup/setup123

		Verify with command nslookup
		nslookup your.domain.name 127.0.0.1
		
		
		Source: https://github.com/jethrocarr/namedmanager
	
