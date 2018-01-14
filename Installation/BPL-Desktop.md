# Blockpool-Desktop Installation

## Windows

### Download Installer

- Download the appropriate BPLClient.Setup.X.X.X-XXbit.exe from [github](https://github.com/blockpool-io/BPL-desktop/releases/latest)
	`pic`
- Run the exe
	`pic`
- Follow on screen prompts to finish installation
	`pics`

### From Source
- todo

## Linux

### Download Installer
- For x64 Debian based Linux download BPLClient_X.X.X_amd64.deb from [github](https://github.com/blockpool-io/BPL-desktop/releases/latest)
- Use your distributions package manager to finish installation

### From Source
In your distributions terminal do the following steps:
- Install Node & npm 
```
sudo apt-get install nodejs
sudo npm install -g n
sudo n 6.9.2
```

- Clone the source code from GitHub
```git clone https://github.com/blockpool-io/BPL-desktop```

- Enter the source code directory
```cd BPL-desktop```

- Install dependencies and compile the client
```
npm install
npm run start
```

# ADD PICS
## OSX
