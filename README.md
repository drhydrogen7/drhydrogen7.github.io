 <script src='https://cdnjs.cloudflare.com/ajax/libs/shaka-player/4.7.6/shaka-player.ui.min.js' crossorigin='anonymous'></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/shaka-player/4.7.6/controls.min.css" crossorigin="anonymous">
  <body bgcolor='black' style='margin:0' oncontextmenu='return false' onkeydown='return false' onmousedown='return false'>
    <style>
    
.shaka-spinner-container { display: none; }
  .video-fill video {
        object-fit: fill cover;
      }
  
   /* Overflow menu style */

.shaka-overflow-menu {
    background-color: rgb(35, 35, 35);
    color: rgb(255, 255, 255);
}

.shaka-overflow-menu button:hover {
    background-color: rgb(45, 45, 45);
}

.shaka-overflow-button-label {
    color: rgb(245, 245, 245);
}

.shaka-current-selection-span {
    color: rgb(202, 202, 202);
}

.material-icons-round {
    color: rgb(230, 230, 230);
}

/* Overflow sub menu style */

.shaka-settings-menu {
    background-color: rgb(35, 35, 35);
    color: rgb(255, 255, 255);
}

.shaka-settings-menu button {
    color: rgb(255, 255, 255);
}

.shaka-settings-menu button:hover {
    background-color: rgb(45, 45, 45);

}

.shaka-bottom-controls {
  display: flex;
  flex-direction: column-reverse;
}



#tglogo {
position: absolute;
right: 80px;
top: 30px;
height: 60px;
width: 100px;
} 
</style>

 <script>
<script type="text/javascript">
	
$(document).ready(function() {
	$('body').bind('cut copy paste', function (e) {
		e.preventDefault();
	})
	$(".code").on("contextmenu", function(e) {
		return false;
	})
})

</script>


<script disable-devtool-auto="" src="https://cdn.jsdelivr.net/npm/disable-devtool"></script>

    <div class="container video-fill" data-shaka-player-container style='position:absolute;z-index: -1;top: 0;left: 0;width: 100%; height: 100%;object-fit:fill cover;'>
      <video autoplay data-shaka-player id='video' poster="#" style='width:100%;height:100%;'>

</video>

    
<img id="tglogo" src="#"> 
<script>
        (async function() {
            // Function to get the value of a query parameter by name
            function getQueryParameter(name) {
                const urlParams = new URLSearchParams(window.location.search);
                return urlParams.get(name);
            }

            // Define multiple manifest URIs and DRM configurations
            const videoConfigs = [

		    {
                    id: 'USANETWORK',
                    manifestUri: 'https://fsly.stream.peacocktv.com/Content/CMAF_OL1-CTR-4s/Live/channel(usa-east)/master.mpd',
                    drmConfig: {
                        clearKeys: {
                            '78ab64fa90f137a697743b5dc27b2f96': 'de4d31c7fc6005ede28abab2a0720a9f'
                        }
                    }
                },
              {
                    id: 'GXR-1',
                    manifestUri: 'https://pull.niues.live/live/stream-9912097_lsd.m3u8?auth_key=1737715055',
                    drmConfig: {
                        clearKeys: {
                            '1eb79728f5994eb18eadbb5b885103de': 'ad8c388edde7bbb722245ec3b019c9aa'
                        }
                    }
                },
              {
                    id: 'GXR-2',
                    manifestUri: 'https://live.ll.ww.aiv-cdn.net/OTTB/dub-nitro/live/clients/dash/enc/wjgklbtvhh/out/v1/659736a1e24c40e4865a80ffd75e7de7/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            '43d1c3b25207ff38b22ccfe17d302367': '7b1f85f6e81059473b114c16a25c829a'
                        }
                    }
                },
               {
                    id: 'TNT_1_GB',
                    manifestUri: 'https://ottb.live.cf.ww.aiv-cdn.net/lhr-nitro/live/clients/dash/enc/wf8usag51e/out/v1/bd3b0c314fff4bb1ab4693358f3cd2d3/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            'ae26845bd33038a9c0774a0981007294': '63ac662dde310cfb4cc6f9b43b34196d'
                        }
                    }
                },
                {
                    id: 'TNT_2_GB',
                    manifestUri: 'https://ottb.live.cf.ww.aiv-cdn.net/lhr-nitro/live/clients/dash/enc/f0qvkrra8j/out/v1/f8fa17f087564f51aa4d5c700be43ec4/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            '6d1708b185c6c4d7b37600520c7cc93c': '1aace05f58d8edef9697fd52cb09f441'
                        }
                    }
                },
                {
                    id: 'TNT_3_GB',
                    manifestUri: 'https://ottb.live.cf.ww.aiv-cdn.net/lhr-nitro/live/clients/dash/enc/lsdasbvglv/out/v1/bb548a3626cd4708afbb94a58d71dce9/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            '4e993aa8c1f295f8b94e8e9e6f6d0bfe': '86a1ed6e96caab8eb1009fe530d2cf4f'
                        }
                    }
                },
                {
                    id: 'TNT_4_GB',
                    manifestUri: 'https://ottb.live.cf.ww.aiv-cdn.net/lhr-nitro/live/clients/dash/enc/i2pcjr4pe5/out/v1/912e9db56d75403b8a9ac0a719110f36/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            'e31a5a81caff5d07ea2411a571fc2e59': '96c5ef69479732ae734f962748c19729'
                        }
                    }
                },
                {
                    id: 'TNT_5_GB',
                    manifestUri: 'https://ottb.live.cf.ww.aiv-cdn.net/lhr-nitro/live/clients/dash/enc/gesdwrdncn/out/v1/79e752f1eccd4e18b6a8904a0bc01f2d/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            '60c0d9b41475e01db4ffb91ed557fbcc': '36ee40e58948ca15e3caba8d47b8f34b'
                        }
                    }
                },
              {
                    id: 'DAZN-LALIGA',
                    manifestUri: 'https://live.ll.ww.aiv-cdn.net/OTTB/dub-nitro/live/clients/dash/enc/wjgklbtvhh/out/v1/659736a1e24c40e4865a80ffd75e7de7/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            '43d1c3b25207ff38b22ccfe17d302367': '7b1f85f6e81059473b114c16a25c829a'
                        }
                    }
                },
              {
                    id: 'DAZN1',
                    manifestUri: 'https://ottb.live.cf.ww.aiv-cdn.net/dub-nitro/live/clients/dash/enc/bmnelo5c7a/out/v1/3ce2cdc4589f46189322bd3717c77957/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            '44dd9cd370b08a868ead115fe84ecfde': 'bff19ab0a51cf14e848389b152913fd0'
                        }
                    }
                },
              {
                    id: 'DAZN2',
                    manifestUri: 'https://ottb.live.cf.ww.aiv-cdn.net/dub-nitro/live/clients/dash/enc/xnk4m9bnxt/out/v1/4ced7b7329a54652b9bb0521ed38bd4d/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            '0eab5a3f3e3b4ba5d42d40ca30d17571': 'f3f061ded9b70e8160590d5802ecda6d'
                        }
                    }
                },
              {
                    id: 'DAZN3',
                    manifestUri: 'https://live.ll.ww.aiv-cdn.net/OTTB/dub-nitro/live/clients/dash/enc/zy1ee5sshp/out/v1/bdcffa69fa3b4f3bb3569c9c73ee1c01/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            'bad8efff688c0dbb3711e4a7114c22a3': '6ba800673b20776c0c850130d45e1920'
                        }
                    }
                },
              {
                    id: 'DAZN4',
                    manifestUri: 'https://live.ll.ww.aiv-cdn.net/OTTB/dub-nitro/live/clients/dash/enc/up7qpwch9b/out/v1/a6d5d1a1287b4893b859c2d6ccf2c65d/cenc.mpd',
                    drmConfig: {
                        clearKeys: {
                            'd27104d427e4f87e75b19395a9f8796b': '723593c70e2d4c4862754398e80168f8'
                        }
                    }
                }, 

              
                // Add more configurations as needed
            ];

            // Function to initialize the video player
            async function init() {
                const id = getQueryParameter('id');
                const config = videoConfigs.find(cfg => cfg.id === id);

                if (!config) {
                    console.error('No valid configuration found for the provided id.');
                    return;
                }

                const video = document.getElementById('video');
                const ui = video['ui'];
                ui.configure({
                    seekBarColors: {
                        base: 'rgba(255,255,255,.2)',
                        buffered: 'rgba(255,255,255,.4)',
                        played: 'rgb(255,0,0)',
                    }
                });

                const controls = ui.getControls();
                const player = controls.getPlayer();

                // Apply DRM configuration to the player
                player.configure({
                    drm: config.drmConfig
                });

                try {
                    await player.load(config.manifestUri);
                    // Mute the video to allow autoplay
                    video.muted = false;
                    await video.play(); // Attempt to autoplay
                } catch (error) {
                    console.error('Error loading manifest or autoplay failed:', error);
                }

                // Replace jQuery with vanilla JavaScript for modifying button text
                document.querySelectorAll('.shaka-overflow-menu-button').forEach(button => {
                    button.textContent = 'settings';
                });
document.querySelectorAll('.shaka-back-to-overflow-button .material-icons-round').forEach(icon => {
                    icon.textContent = 'arrow_back_ios_new';
                });
            }
                

            document.addEventListener('shaka-ui-loaded', init);
// Display a pop-up message when the page starts
            
        })();
            
    </script>
  <a href="#" target="_blank">
<span style="position: absolute; z-index: 100; top: 6px; left: 5px; height: 30px; width: 100px; color: rgb(204, 204, 204); border: 2px solid rgb(204, 204, 204); padding: 1px 0px; border-radius: 2px; text-align: center;">
Join us
</span>
</a>

