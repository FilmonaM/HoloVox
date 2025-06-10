| title       | author  | description                                                                                                   | created_at |
| :---------- | :------ | :------------------------------------------------------------------------------------------------------------ | :--------- |
| HoloDisplay | Filmona | the holovox is a spinning LED display that shows 3D voxel images by abusing the persistence of vision effect. | 06-08-2025 |
Total Time: 6.5 hours

June 8th - Starting out:
[Doom on a Volumetric Display - YouTube](https://www.youtube.com/watch?v=na7pvihXhYs)
I came across this video a couple months ago showcasing doom being played live on a volumetric display. This sparked my interest in hologram technology and other futuristic tech in general. So I wanted to take this opportunity to build my own version of this which reduces the cost while also making it a little more accessible in size and buildability.

Today, I went back through the youtube channel and watched all of the videos on the vortex and other volumetric displays and also found this video -[Vortex Assembly - YouTube](https://www.youtube.com/watch?v=pcAEqbYwixU) - which serves as a good starting point. I also went through his GitHub repo and explored his code and hardware docs. I tried out the virtex simulator and it took a lot of effort to get set up, but it was an amazing proof of concept thing where I was able to visualize the voxel buffer with the virtex gui.

![[Pasted image 20250609193209.png]]
Time Spent = 4 hours

June 9th - Research, goals and first design:
- [ ] successfully render anything
- [ ] doesn't shake violently
- [ ] make easy to use
- [ ] a software to make converting to 3d voxel easier(??)

Today I spent most of the time taking notes on the logic and system behind what a volumetric display is. I  organizing all my notes into sections: display logic, hardware, timing, and structure. I also went deeper into how voxel data is represented and how it gets turned into motion through timing math.

I started looking at other designs like [PropHelix](https://www.instructables.com/PropHelix-3D-POV-Display/) to see what kinds of parts and frame styles people were using. I'm leaning toward using a HUB75 LED panel instead of strips because although it may be heavier it has denser LEDs.

I also sketched out my first idea for what my holodisplay could look like with safety in mind. I think this setup instead of a dume might be a bit safer but I feel like I can't really make any decisions until I figure out how big I want this to be.

![[Pasted image 20250609194846.png]]time spent = 2.5 hrs