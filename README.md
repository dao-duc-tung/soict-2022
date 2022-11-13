# SoICT 2022

This repository serves the tutorial session for SoICT 2022.

SoICT 2022 is an international symposium covering significant research areas that include AI Foundations and Big Data, Network Communication and Security, Image and Natural Language Processing, Software Engineering and Digital Technology, Blockchain and Financial Technology trends.

## Setup Wandb

There are 2 ways to setup your working environment

- Option 1: To use Wandb cloud server
- Option 2: To use self-hosted Wandb server

I recommend you to use the option 1 to quickly start the tutorial.
The option 2 is to setup your environment at local after you understand how Wandb's main features work.

### Option 1: Wandb cloud server

- Setup Wandb account
  - Create a Wandb account and login
  - Get API key at <https://wandb.ai/authorize>
- Setup environment
  - Create a Python 3.9 environment by using `conda`, `venv`, etc.
  - Run
    ```bash
    pip install -r requirements.txt
    wandb login --cloud
    # Paste the API key when asked
    ```

### Option 2: Self-hosted Wandb server

This section guides you to setup your own Wandb server.

- Setup Wandb account
  - Create a Wandb account and login
  - Get API key at <https://wandb.ai/authorize>
- Setup environment
  - Install docker
  - Create a Python 3.9 environment by using `conda`, `venv`, etc.
  - Run
    ```bash
    pip install -r requirements.txt
    wandb server start
    # Wait for 30s
    # Paste the API key when asked
    ```
  - Go to <http://localhost:8080/signup>, register an account with username `demo` and password `demodemo` and login
  - Follow [this](https://docs.wandb.ai/guides/self-hosted/local#generate-a-free-license) to generate a free license and add it to the local server
  - Get _local API key_ at <http://localhost:8080/authorize>
  - Relogin
    ```bash
    wandb login --host=http://localhost:8080 --relogin
    # Paste the local API key when asked
    ```
- Teardown
  ```bash
  wandb server stop
  docker volume rm wandb
  ```

## Run tutorial

You can:

- Run tutorial in the file [tutorial/tutorial-01.ipynb](tutorial/tutorial-01.ipynb) in this repo
- See the project's result at [my Wandb project](https://wandb.ai/tungdao/soict-2022)

## Useful links

- [SoICT 2022](https://soict.org/)
- [Tutorial slides](https://docs.google.com/presentation/d/1kWUM4mDHcnzL_CmVukkxbc7AhOzjhju9RHC2fuZbJ6I/edit?usp=sharing)

## License

Distributed under the MIT License. See LICENSE for more information.

## Contact

Tung Dao - [LinkedIn](https://www.linkedin.com/in/tungdao17/)

## Acknowledgements

- [Weights & Biases](https://wandb.ai/site)
- [ml-ops.org](https://ml-ops.org/)
- [AIEngineer.net](https://aiengineer.net/)
