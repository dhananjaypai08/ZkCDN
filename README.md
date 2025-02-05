# Decentralized Content Distribution
#### A Dapp providing secure content distribution by leveraging Zero knowledge proofs and Soul Bound Tokens. We provide a dynamic indexing dashboard and use generative AI to query your subgraph data using asynchronous subgrounds 

### Deployments
- zkcdnGraph Subgraph : [https://thegraph.com/studio/subgraph/zkcdngraph/](https://thegraph.com/studio/subgraph/zkcdngraph/)


### Setting up the project locally

First clone the project
1.) Frontend setup
```sh
cd zkcdn
npm i
npm run dev
```
2.) Off chain compute (wsl/linux based os) and 1 offchain Generative AI model
```sh
cd off-chainPy
python -m venv env
source env/bin/activate
pip install -r requirements.txt
cd proofs
python main.py
```
3.) Running the 2nd offchain ( The graph protocol's python subground package)
```sh
cd off-chainPy
python -m venv env
source env/bin/activate
pip install -r requirements.txt
cd subgrounds
python main.py
```
Done! you're frontend is now running on [http://localhost:5173/](http://localhost:5173/)

### Tools
- Reactjs
- Zokrates(Circuit building and compilation)
- FastAPI (zkproofs compute off chain)
- Subgrounds
- The graph protocol sdk

### Open for contributions
Open for contributions, please drop a fix/change with details in the PR
