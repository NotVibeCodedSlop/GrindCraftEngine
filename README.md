# GrindCraftEngine
A engine for GrindCraft
## 1. Setup
Basically in the index.html you can see a `<script>` object, there is `let assetRoot = "./game/";`
You can change that to any path that has your assets of GrindCraft.
For assets go to [GrindCraft](https://grindcraft.com/game/index.html) and open devtools. Then wait untill it loads and copy all as URLs
then in some way delete the `?636391` and other params in the URLs and get every one of them
idk you can open Kate, paste in the URLs and CTRL+F replace with RegEx mode find `\?.*` replace ``
then save and run `wget -i urls.txt -nH --cut-dirs=0 --force-directories` to fetch all of them, maybe clean up after as it litears into the `CWD` for no reason except why not.
Then move it into your GrindCraft folder
it should look like this: 
```
/
├── index.html          # Your engine entry point
├── README.md           # This documentation
└── game/               # Root folder for assets (Set assetRoot = "./game/" or whatever you pick, if it's on a different server you can too put it here)
    ├── data/           # XML data files
    ├── img/            # Images
    └── sounds/         # Sounds and music
```
Now you need a http server for it, just don't well... put the copyrighted assets on the internet.
I just `python -m http.server 8000`
## 2. Play
Beacuse this engine uses the same file structure the original you can now simply play or edit the textures.
You can even change the language if you change the ```const mapRes = await fetch(`${assetRoot}data/maps/en/${currentMapName}.xml`);``` line.
