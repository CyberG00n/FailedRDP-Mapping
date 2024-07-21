<a href="https://ibb.co/8Mh5gzy"><img src="https://i.ibb.co/9nMTHwx/banner-2.png" alt="Failed-RDP Mapping" border="0" align="center"></a>

<h2 align="center">Mapping out all the failed RDP request, lol.</h2>

<h3 align="center"> About.</h3>

This project was not long to implament but it did provide me with valuable skills. Essentially, it is setting up a honey pot on the internet, and whenever someone tries to log in and fail, it logs that down. With the log information I am able to obtain their IP address and map out where they are. This was implamented in Microsoft Azure!
<a href="https://ibb.co/SJZZDwM"><img src="https://i.ibb.co/BwYYH2Q/Chart.png" alt="Chart" border="0"></a>

<h3 align="center">Documentation</h3>

First things first, I set up a Microsoft Azure account. If it is your first time signing up, Microsoft does give you a free 200$ credit you can use. I used that and didn't use all of it; it's pretty neat.

We then create the honey pot and deactivate all of its firewall settings. This ensures the VM is discoverable and enticing for somebody trying to get in. I set up a very secure password to ensure no break-ins are possible!
<h3 align="center" style="color: red" > THIS IS THE VIRTUAL MACHINE </h3>
<a href="https://ibb.co/By0cbd0"><img src="https://i.ibb.co/JvDmV0D/firewlal.png" alt="firewlal" border="0"></a>

After the VM is set up, we run Powershell ISE and plug in the code to check the event viewer for failed login attempts (ID 4625). This runs consecutively, and if it captures anything, it sends it over to log analytics
<a href="https://ibb.co/RH2z95y"><img src="https://i.ibb.co/Hg7nVJd/VM.png" alt="VM" border="0"></a>

This is where the fun begins; it sends the information, including everything from the longitude and latitude to the country of origin. We take this raw data and filter it out in log analytics. This is then sent to sentinal, where it is finally mapped out. If you're curious about the error, that is because I ran out of IP calles. In the next image you can see why lol.
<a href="https://ibb.co/wWTsPnt"><img src="https://i.ibb.co/J7NQGYZ/Log.jpg" alt="Log" border="0"></a>

Mapping the information out wasn't hard; you create and add a new workbook, and then it can map it out for you! This part is also funny to me because I left the VM to run and I come back to find that 3 bots where trying to bruteforce thier way into my VM. They tried at least 2.5k of those attempts.s They eventually used up all my API calls for GEOIP and thats why it would give me that error.
<a href="https://ibb.co/GWTVqNv"><img src="https://i.ibb.co/Htdrj3D/Map.jpg" alt="Map" border="0"></a>

This project was a little programming, except for SQL and some Java, but it was reasonably straightforward. The tutorial I went through was outdated, so some things changed. If you would like to do this project, here is the link: https://www.youtube.com/watch?v=RoZeVbbZ0o0\&t=2759s
 If you have any questions, please don't hesitate to contact me. I struggled through the part where he pares the raw data, as Azure changed the Custom Log part.

<img src="https://media.giphy.com/media/oobNzX5ICcRZC/giphy.gif?cid=ecf05e47ggfln5y0qhz7h3do3ybue8n73amijws5ra2pob31\&ep=v1\_gifs\_search\&rid=giphy.gif\&ct=g
" width="350" align="center">