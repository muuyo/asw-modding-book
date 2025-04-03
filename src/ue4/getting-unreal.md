# Installing Unreal Engine

<hr>

Arc System Works has customized various aspects of Unreal Engine 4 to suit their needs.

This means that although we can install the plain vanilla UE4 and use that to make mods, we'd be missing on key features needed to make them work properly. Thankfully, Ryn has reverse-engineered several of these changes and implemented some of the key features we require into custom UE4 builds.

You can find the download links below. Just pick the one matching the game you wish to mod. Note that the exact version is important; you cannot do things like use UE4.27 to mod DBFZ.

| Game                          | Engine                                                                                                   |
| ----------------------------- | -------------------------------------------------------------------------------------------------------- |
| Dragon Ball FighterZ          | [Unreal Engine 4.17](https://1drv.ms/u/s!ApT7KvOr_B0hy4ZgwT3lHcwhu3MVSA?e=cTrwqV)                        |
| Guilty Gear \-Strive\-        | [Unreal Engine 4.25 Plus](https://drive.google.com/drive/u/0/folders/16hIM2Gy7V2Vcc3cpj10nY4emUhqmJwd7)  |
| DNF Duel                      | [Unreal Engine 4.25](https://1drv.ms/u/s!ApT7KvOr_B0hkPgRVEhN1MsPEpnAeA?e=bPFdsf)                        |
| Granblue Fantasy Versus       | [Unreal Engine 4.21](https://1drv.ms/u/s!ApT7KvOr_B0hkPgWb5AjxrUapJcYmQ?e=79mVYA)                        |
| Granblue Fantasy Versus Rising | [Unreal Engine 4.27](https://drive.google.com/file/d/1SnX9rcMxeHP82GojHocdLUux2Sa0qZG1/view?usp=sharing) |

The EXE you're going to want to launch to start the project is typically in `Engine/Binaries/Win64/`. 

The Guilty Gear -Strive- editor may receive periodic patches in another archive. You'll need to update it using the steps on the [next page](./custom-project.md) for actually setting up the editor.

## STRIVE SPECIFICS

Strive has a bit of extra setup that you'll have to do to get it working!  
First, you'll want to download all 3 files from the above link.  
Extract `GGSTCookedEditor` anywhere, and you'll have 2 folders: RED and Engine.  
Extract `CookedEditor_Patch` into the same folder, merging RED with RED and Engine with Engine.  
Drag the Content_Patch contents into RED, then you can go into `RED/Binaries/Win64` to launch the Unreal editor.  
To make a new project to do your own work in, you'll have to follow the directions on the [custom project page](./custom-project.md).

currently, there's an updated ver of the CharaMaterial folder as well; use this or things bug out.
download from this repo [here](./files/CharaMaterial.rar) then extract it like the above; go into RED/ (your project's folder) then copy Content into there, replacing files when prompted.