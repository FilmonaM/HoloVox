
## links:
- https://www.youtube.com/watch?v=pcAEqbYwixU
- https://www.youtube.com/watch?v=na7pvihXhYs 
- [PropHelix - 3D POV Display : 8 Steps (with Pictures) - Instructables](https://www.instructables.com/PropHelix-3D-POV-Display/)
- [I am looking for a 64x128 led matrix display capable of hitting very high refresh rates > 1.5khz : r/FastLED](https://www.reddit.com/r/FastLED/comments/1fqe0nl/i_am_looking_for_a_64x128_led_matrix_display/)
- [DOOM On A Volumetric Display | Hackaday](https://hackaday.com/2024/09/09/doom-on-a-volumetric-display/#more-705955#:~:text=The%20base%20contains%20a%20DC,might%20not%20even%20be%20enough)
- [Voxel Doom - The Doom Wiki at DoomWiki.org](https://doomwiki.org/wiki/Voxel_Doom)
- [MagicaVoxel](https://ephtracy.github.io/)
- [Photonics Challenger: Transparent 3D Volumetric POV (PHABLABS) : 8 Steps (with Pictures) - Instructables](https://www.instructables.com/Transparent-3D-Volumetric-POV/)
- [Voxel - Wikipedia](https://en.wikipedia.org/wiki/Voxel)

--- 
### display logics
- voxel = 3D pixel = visible only b/c persistence of vision (POV)
- each LED = vertical voxel slice
- as strip rotates, blinks are timed so each LED represents many points in 3D space
	- 1 LED × 360° = 360 potential voxels  
	- 64 LEDs → 64 × 360 = 23,040 voxels  
coordinate system:
- height = LED #
- angle = rotation slice
- radius = fixed 
- rendered in cylindrical space: (θ, z)
- voxel data is stored in a buffer as voxelBuffer(angle)(height)
	- holds a 3-byte color value (R, G, B)

### hardware

microcontrollers or rasberry pi (or a both) for quick real time control
- Teensy - powerful and fast 
- arduino and/or esp32
- rasberry pi 4/5    

brushless dc motor + esc with a hall effect sensor and magnet for syncing

LED strips - dotstar or hub75

Power:
- Wireless with coils (cooler and potential for more)
- slipring  

### timing math
- 1 full frame = 1 full rotation
- sync signal from hall effect sensor (triggers "angle 0")
- time between triggers = full frame duration (T)
- T divided into angular steps (360)
	- 20 RPS = 50 ms --> 50 ms / 360 = 139 microseconds per slice
	- update must occur within the window of the slice 
### structure ideas
- 3d printed casing
- obviously clear viewing cover thing
	- removable panels
	- acrylic dome
- weighted bearings to keep stuff down
- a lot of good magnets and superglue to ensure everything stays together cause this is kinda dangerous