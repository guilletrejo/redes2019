all : setup delete_routes 

setup:
	docker-compose -p tp4 up -d

clean:
	docker network prune
	docker-compose -p tp4 down

delete_routes:
	docker exec -ti tp4_r1_1 ip -6 route del default;
	docker exec -ti tp4_r1_1 ip route del default;
	docker exec -ti tp4_r2_1 ip -6 route del default;
	docker exec -ti tp4_r2_1 ip route del default;
	docker exec -ti tp4_r11_1 ip -6 route del default;
	docker exec -ti tp4_r11_1 ip route del default;
	docker exec -ti tp4_r12_1 ip -6 route del default;
	docker exec -ti tp4_r12_1 ip route del default;
	docker exec -ti tp4_r21_1 ip -6 route del default;
	docker exec -ti tp4_r21_1 ip route del default;
	docker exec -ti tp4_r22_1 ip -6 route del default;
	docker exec -ti tp4_r22_1 ip route del default;
	docker exec -ti tp4_nginx_1 ip -6 route del default;
	docker exec -ti tp4_nginx_1 ip route del default;
	docker exec -ti tp4_apache_1 ip -6 route del default;
	docker exec -ti tp4_apache_1 ip route del default;
	docker exec -ti tp4_nginx_1 ip route add default via 192.2.2.2;
	docker exec -ti tp4_nginx_1 ip -6 route add default via aaaa:2:2::2;
	docker exec -ti tp4_apache_1 ip route add default via 192.1.8.2;
	docker exec -ti tp4_apache_1 ip -6 route add default via aaaa:1:8::2;