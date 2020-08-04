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

-------------

Patch notes
-----------

Some changes are required from stock LineageOS in order to fix some issues.

Frameworks base requires this commit to fix Always On Display not entering deep sleep:

	https://github.com/crdroidandroid/android_frameworks_base/commit/20e5811d89084a9bf8002e08e513273c94024341

Open source display stack requires a CAF display HAL. Lineage display HAL is incompatible, the required modification has been made to the manifest.
