# Run DeepSeek Locally with Docker-Compose

Running DeepSeek locally with Docker-Compose is possible with a Mac, though a lighter-weight implementation of the model is recommended.

This will take you through how to run DeepSeek on localhost with a web-ui interface. 

![alt text](image.png)

## Steps

1. Install [Ollama](https://martech.org/how-to-run-deepseek-locally-on-your-computer/)
2.  Pick a model based on your hardware:
```
ollama pull deepseek-r1:8b  # Fast, lightweight  

ollama pull deepseek-r1:14b # Balanced performance  

ollama pull deepseek-r1:32b # Heavy processing  

ollama pull deepseek-r1:70b # Max reasoning, slowest
```
3. Test the model locally via the terminal 
```
ollama run deepseek-r1:8b
```

4. Install [Docker](https://www.docker.com/get-started)

5. Install [Docker-Compose](https://formulae.brew.sh/formula/docker-compose)

6. Create Docker-Compose file as seen in this repo. 

7. Open the docker app and run `docker-compose up -d`

8. Visit `http://localhost:3000`

