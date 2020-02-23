LineageOS 17.1 for Xiaomi Mi Mix 3 5G
------------------------------------

Create directories

	$ mkdir lineage-17.1
	$ cd lineage-17.1

Init lineage:

	$ repo init -u git://github.com/LineageOS/android.git -b lineage-17.1
  

Download and move the manifest xml for the device you want to .repo/local_manifests/

Then sync up with this command:

	$ repo sync

-------------
 
_Building from source_
---------------

	$ . build/envsetup.sh
	$ lunch lineage_andromeda-userdebug
	$ mka bacon
