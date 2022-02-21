# PublicBotProfiles
A collection of Artifulate public bot profile models

## Tool requirements 

Note that you will need a Java Runtime for executing a mdeshell shell script

Artifualte bot profiles require MDESHELL (https://github.com/vorachet/mdeshell) to perform model definition and transformation tasks.

## Setup your workspace

Assume your workspace is located in ~/git

Clone MDESHELL tools and environment 
```
cd ~/git

git clone git@github.com:vorachet/mdeshell.git

```

Clone Artifulate Bot Profile Models
```
cd ~/git

git clone git@github.com:Artifulate/PublicBotProfiles.git

```

Create a softlink of PublicBotProfiles project to MDESHELL
```
cd ~/git/mdeshell/projects

ln -s ~/git/PublicBotProfiles/projects/artifulate_bot_profiles .

```

Your folder structure in MDESHELL environment 

```
.
├── README.md
├── libs                       # MDESHELL Libs
├── projects
│   ├── <Example Projects>     # MDESHELL example projects
│   ├── artifulate_bot_profiles -> /<YourUserHome>/git/PublicBotProfiles/projects/artifulate_bot_profiles
│       └── inputs
│           ├── *.flexmi       # Bot profile models
│           ├── *.egx          # Generation file - DON'T EDIT
│           ├── *.emf          # Metamodel files - DON'T EDIT
│           └── templates
│               ├── *.egl      # Generation templates - DON'T EDIT
└── run.sh                     # MDESHELL runner script

```

## Generate Artifulate Bot Profile Configuration Files

Run MDESHELL runner script. The script will require you enter the number of target project that needs to be computed by MDESHELL. With this example, enter number 3, where artifulate_bot_profiles is located.
```
cd ~/git/mdeshell

./run.sh

Choose project number:
1) 01_getting_started	    3) artifulate_bot_profiles
2) 02_my_shell_program
#? 3
\nProject: artifulate_bot_profiles (/<YourUserHome>/git/mdeshell/projects/artifulate_bot_profiles)
\nGenerating...
\nDone! Note that location of generated files will be specified by your .egx files\n

```

Bot Profile configuration files will be generated in `~/git/PublicBotProfiles/projects/artifulate_bot_profiles/*`

```
cd ~/git/PublicBotProfiles/projects/artifulate_bot_profiles
.
├── generated
│   ├── DRIVER_SERVICE_BOT.json
│   └── SIMPLE_ECOMMERCE_BOT.json
├── inputs/*
└── outputs/*

```