```shell
docker build -t my-readme-ai .
```

Run the docker container locally
```shell
docker run -it \
-e OPENAI_API_KEY=$OPENAI_API_KEY \
-v "$(pwd)":/app my-readme-ai:latest \
--context-window 64000 \
--model gpt-4o \
--rate-limit 1 \
--tree-depth 5 \
-r .
```

Or with chatGPT-3.5
```shell
docker run -it \
-e OPENAI_API_KEY=$OPENAI_API_KEY \
-v "$(pwd)":/app my-readme-ai:latest \
--context-window 8000 \
--model gpt-3.5-turbo \
--rate-limit 1 \
--tree-depth 5 \
-r .
```