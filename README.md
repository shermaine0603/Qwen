# Qwen
```sh
docker build . -t rag
```

```sh
docker rm rag
docker run --gpus all -it -v /home/raus/Qwen:/pic --name rag rag
```

```sh
docker run --gpus all -it -e PYTORCH_CUDA_ALLOC_CONF=expandable_segments:True -v /home/raus/Qwen:/pic --name rag rag
```

Exit the docker container, then use this line to transfer the test file to inside the docker.
```sh
docker cp Qwen_test.py rag:Qwen2.5-VL-3B-Instruct-AWQ/Qwen_test.py
```

Get docker container id from:
```sh
docker ps -a
```

Start the container
```sh
    docker start rag
```

```sh
docker exec -it rag bash
```

```sh
cd Qwen2.5-VL-3B-Instruct-AWQ
```

```sh
python3 Qwen_test.py
```
