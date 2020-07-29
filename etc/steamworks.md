## steam P2P with UNET 
* https://www.reddit.com/r/Unity3D/comments/7uvimi/how_to_use_unet_hlapi_with_steam_p2p_example/
* https://blog.spacewavesoftware.com/gamedev/2017-10-28-unity-unet-hlapi-and-steam-p2p-networking/
* https://github.com/rempelj/unet-steamworks

## Publish my app
* partner link : https://partner.steamgames.com/home (need to sign up)
* Add other users to our application : https://partner.steamgames.com/doc/gettingstarted/managing_users
* Tutorial link : https://partner.steamgames.com/doc/sdk/uploading

## Upload my app 
* can upload zip file (less than 256MB) through steamworks page 
* How to move to th steam works page
![image](https://github.com/westside/study/blob/master/images/steamworks-1.PNG)
* download steamworks sdk (to upload) : https://partner.steamgames.com/downloads/steamworks_sdk_142.zip
* https://partner.steamgames.com/doc/sdk/uploading
* video tutorial: https://www.youtube.com/watch?v=SoNH-v6aU9Q

* run sdk\tools\ContentBuilder\builder\steamcmd.exe
```
login userid
run_app_build_http ..\scripts\app_build_966420.vdf
quit

```
* or use bat file sdk\tools\ContentBuilder\run_build.bat
* be sure to check appId and depoId
   
