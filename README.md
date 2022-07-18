# build-revanced-collab
Allows to build revanced on Google Collab, with option to include and exclude patches!
## Patches for youtube app
 
**Patches which are enabled by default:-**
>(exclude)
```
- hide-infocard-suggestions
- video-ads
- general-ads
- seekbar-tapping
- swipe-controls
- microg-support
- custom-playback-speed
- hide-cast-button
- amoled
- hide-autoplay-button
- minimized-playback
- premium-heading
- return-yiutube-dislikes
- custom-branding
- disable-fullscreen-panels
```

**Pathces which need to specified :-**
>(include)
```
- hdr-auto-brightness
- autorepeat-by-default
- enable-debugging
- old-quality-layout(Incompatible with latest versions)
- enable-wide-searchbar
```

## Patches for youtube music app
```
- music-video-ads
- exclusive-audio-playback
- codecs-unlock
- background-play
- upgrade-button-remover
- tasteBuilder-remover
```
>Note: The main command whoch you need to edit is 
`!additional_args="" what_to_patch="youtube" sh -c "$(curl https://raw.githubusercontent.com/XDream8/revanced-creator/main/patch.sh)"`
>The commands present above in the collab is to install java and to download apk,patches,cli etc.

# How to include or exclude patches?
**We can include patches using -i patch_name in the additional_args.**
so if i want to include auto hdr brightness patch, we will write:-
```!additional_args="-i auto-hdr-brightness" what_to_patch="youtube" sh -c "$(curl https://raw.githubusercontent.com/XDream8/revanced-creator/main/patch.sh)"```

**Similarly, we can exclude patches by using -e in the additional_args.**
so if we want to remove amoled patch, we will write:-
```!additional_args="-e amoled" what_to_patch="youtube" sh -c "$(curl https://raw.githubusercontent.com/XDream8/revanced-creator/main/patch.sh)"```

**How to add and exclude one, or multiple patches?**
in this case we will write:-
```!additional_args="-e amoled -e video_ads -i hdr_auto_brightness -i enable_debbuging" what_to_patch="youtube" sh -c "$(curl https://raw.githubusercontent.com/XDream8/revanced-creator/main/patch.sh)"```



## Select between Youtube and Youtube Music.
### if you want to patch the youtube app, write "youtube" in what_to_patch="youtube"
### if you want to patch youtube music app. write "youtube-music in what_to_patch="youtube_music"
