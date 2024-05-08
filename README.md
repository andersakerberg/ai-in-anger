# ai-in-anger

## Setup instructions of how to easily get started with local LLM and putting a UI ontop of it

1. Download and install https://ollama.com/
2. After you have set it up make sure the current curl works

```sh
curl http://localhost:11434/api/chat -d '{
  "model": "llama3",
  "messages": [
    { "role": "user", "content": "why is the sky blue?" }
  ]
}'
```

If not read the docs on ollama.com

## Use in VSCode directly

1. Install continue extension from VSCode https://github.com/continuedev/continue
2. Follow the video instructions below

[![IMAGE ALT TEXT](http://img.youtube.com/vi/_mcv_rcC0mk/0.jpg)](http://www.youtube.com/watch?v=_mcv_rcC0mk "Setup continue against LLM")

<video src="setup-continue.mp4" width="560" height="auto" controls></video>


## Use OpenWebUI (like chatGPT)

1. Go to https://github.com/open-webui/open-webui
2. Make sure you have docker installed
3. Run the following command in your terminal

```sh
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

4. Go to http://localhost:3000
5. Done! You can now query against your local model!
