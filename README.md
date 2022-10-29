# SOICT 2022

## Setup environment

- Setup wandb account
  - Create a wandb account
  - Get API key [here](https://wandb.ai/authorize)
  - Follow [this](https://docs.wandb.ai/guides/self-hosted/local#generate-a-free-license) to generate a free license
- Setup dev env
  - Install docker
  - Create a Python 3.9 dev env
  - Run
    ```bash
    pip install -r requirements.txt
    wandb server start
    # Wait for 30s
    # Paste the API key when it asks for
    ```
  - Go to <http://localhost:8080/signup>, register an account with username `demo` and password `demodemo`
  - Follow [this](https://docs.wandb.ai/guides/self-hosted/local#add-a-license-to-your-local-host) to add the generated license above
  - Get local API key [here](http://localhost:8080/authorize)
  - Relogin
    ```bash
    wandb login --host=http://localhost:8080 --relogin
    # Paste the local API key when it asks for
    ```
- Teardown
  ```bash
  wandb server stop
  docker volume rm wandb
  ```
