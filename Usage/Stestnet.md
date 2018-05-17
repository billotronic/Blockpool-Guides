# Upcoming Public Testnet TEST	

The next major test for Blockpool will be on a new chain and from a different branch on github then that of a standard install. These are the instructions for setting up a node for this testnet test.

NOTE: at this time you are unable to use BPLcommander for this install.

### Create a user for the node

1. Use the `adduser` command to add a new user to your system. Be sure to replace username with the user that you want to create.

	`adduser username`


2. Set and confirm the new user's password at the prompt. A strong password is highly recommended!


3. Follow the prompts to set the new user's information. It is fine to accept the defaults to leave all of this information blank.


4. Use the usermod command to add the user to the sudo group.

	`usermod -aG sudo username`
	
	Again replacing username with the name used in step #1


5. Switch to the new user

	`su - username`


### Install essentials

```
sudo apt-get update
sudo apt-get install -y curl build-essential python git
```

### Install Node.js (min version: 6.9.2)

```
sudo apt-get install -y nodejs
sudo apt-get install -y npm
sudo npm install -g n
sudo n 6.9.2
```

### Install grunt-cli (globally)

```
sudo npm install grunt-cli -g
```

### Install PostgreSQL (min version: 9.5.2)

```
sudo apt-get install -y postgresql postgresql-contrib
sudo -u postgres createuser -P --createdb $USER
createdb ‘Database Name’  (this should match with the database name from config file)
```

### Clone BPL Node repository

```
git clone https://github.com/blockpool-io/BPL-node.git   
cd BPL-node
git checkout testnet
```

### Install node modules

```
sudo apt-get install -y libpq-dev
npm install libpq secp256k1
npm install
sudo npm install forever -g
```

### Add configurations for your node

```
	Change the following in config.testnet.json :
“address“: “set your IP”
“database”: “set database name”
“user”: “set database user”
“password”: “set database password”
“list”: [
	{
		“ip”: “set your IP address”
		“port”: “set the port on which your node will be running”
	},
{
		“ip”: “Set seed node IP address”
		“port”: “set the port on which seed node will be running”
	}
]
```

### Launch BPL node

```
To launch BPL node on testnet:
forever start app.js -c config.testnet.json -g genesisBlock.mainnet.json
```
To stop the node:

```forever stop 0```

To view the bpl log: (assuming location is BPL-node/)

```tail -f logs/bpl.log```