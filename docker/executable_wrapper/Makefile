image:
	cp ./../../contrib/foundationdb/lib/libfdb_c.so ../../build/programs/
	cp ./app/run.sh ../../build/programs/
	docker build --network=host -t minhthucdao1/byconity-server ../../build/programs -f Dockerfile
image_pull:
	docker pull minhthucdao1/byconity-server:v0.1
image_push:
	docker tag minhthucdao1/byconity-server:latest minhthucdao1/byconity-server:v0.1
	docker push minhthucdao1/byconity-server:v0.1
run:
	docker run -it --network host --name dao_tso minhthucdao1/byconity-server 
debug_image:
	docker exec -it byconity-tso /bin/bash
prepare_config:
	./config/prepare_config.py
