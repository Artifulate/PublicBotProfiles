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

cd PublicBotProfiles


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
│               ├── *.egl      # Temaplte files - DON'T EDIT
└── run.sh                     # MDESHELL runner script

```