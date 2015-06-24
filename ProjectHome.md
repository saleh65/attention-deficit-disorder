ADD is a physical memory anti-analysis tool designed to pollute memory with fake artifacts.  This tool was first presented at Shmoocon 2014.  Please note that this is a proof of concept tool.  It forges OS objects in memory (poorly).  It would be easy (very easy) to beat with better tool development.  The tools would only need to provide better sanity checks of objects discovered during scanning.  In that case, further development on ADD would be needed to beat new versions of forensics tools.

The tool currently works only against Windows 7 SP1 x86.

Huge portions of the driver code were based on the Windows DDK Sioctl driver code sample(because honestly, who wants to build device manager PnP code?).

Haven't started source code versioning yet, just wanted to get the code out there so people can play with it.  Started a Google code project for this before I remembered they restricted downloads on new projects (I guess all downloads are disabled now).

FYI, there are places I don't do error checking where "real" programmers probably would.  I'd like to point out that this is a PROOF OF CONCEPT tool.  I don't think I'd run it on a target system without further testing and code auditing.  Load the driver on a production system at your own risk.  I haven't had any bugchecks with it yet, but YMMV.

Driver:
http://www.mediafire.com/download/v4jop3qois3gv4t/add-driver.zip

User Agent:
http://www.mediafire.com/download/see7o8rtnuwstp9/ADD_File.zip

Reference Memory Image (with faked artifacts):
http://www.mediafire.com/download/vvb0dbg2g2h1ukm/ADD-ref-image.zip

Shmoocon Slides:
http://www.mediafire.com/view/h7bmcscbtyaeb6r/ADD_Shmoocon.pdf
