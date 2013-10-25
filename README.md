
![alt tag](https://raw.github.com/ajwinn/Zebra/master/logo.jpg)

Zebra
=====

The two-toned beast you've been waiting for to handle both YouTube &amp; Vimeo.


# _Project_

_Description: Using two separate APIs with YouTube and Vimeo is a pain. Use one. Brought to you by a guy at Zerply._

## Project Setup

_Just do two things:_ 

1. _Requirements: Include zebra.js in the `<head>` and make a new Zebra instance_
2. _See demo [here](http://j.mp/16xheuX). _

## Settings

_You have access to two sets of configuration variables (YouTube &amp; Vimeo) when you create your the Zebra object. Here are the defaults:_

### Assuming you have HTML like

1. `<div id="youtube_player"></div>`

or

2. `<div id="vimeo_player"></div>`

### Fully Loaded YouTube Configuration/Instantiation

    var player = new Zebra({
      url:'https://www.youtube.com/watch?feature=player_embedded&v=PaOaEjdCkoY', 
      target:'yt_player', 
      width:'400',
      height:'225', 
      playerVars:{
        'autohide':2,
        'autoplay':0,
        'cc_load_policy':'',
        'color':'white',
        'controls':1,
        'disablekb':0,
        'end':'',
        'iv_load_policy':1,
        'list':'',
        'listType':'',
        'playlist':'',
        'loop':0,
        'modestBranding':'',
        'origin':'',
        'rel':0,
        'showinfo':1,
        'start':'',
        'theme':'light',
      },
      duringUpdateTime: duringUpdateTime,
      duringNote: duringNote,
      duringTimeline:duringTimeline,
      onSetNote: onSetNote,
      onRemoveNote: onRemoveNote
    });

### Fully Loaded Vimeo Configuration/Instantiation

    var player = new Zebra({
      url:'http://player.vimeo.com/video/23469566', 
      target:'v_player', 
      width:'400',
      height:'225', 
      playerVars:{
        'autoplay':0,
        'autopause':1,
        'badge':1,
        'byline':1,
        'color':'', //use hex wihtout #
        'loop':0,
        'portrait':1,
        'title':1
      },
      duringUpdateTime: duringUpdateTime,
      duringNote: duringNote,
      duringTimeline:duringTimeline,
      onSetNote: onSetNote,
      onRemoveNote: onRemoveNote

    });

## _Common Commands_

    player.play()

    player.pause()
    
    player.addNote({
      start:#,
      end:#,
      text:'string'
      callback:function(){}
    })
    
    player.removeNote(#_start_seconds)

    player.seekTo(#_seconds)


## _Need More Power?_

_The global variables of the native APIs are still there. Play with the original players using `youtube_player` and `vimeo_player`. Examples if you're familiar with the native APIs: `youtube_player.playVideo()` or `vimeo_player.api('play')`_


## License

_You should use Zebra however you want. I could probably go copy and paste some kind of license thing here, but honestly, I just want you to make me famous._