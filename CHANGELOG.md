# Version 1.2.6 - Nov 15, 2016
## Bug Fixes
    * Fixed IOSResolver errors when iOS support is not installed.
    * Added fallback to "pod" executable search which queries the Ruby Gems
      package manager for the binary install location.

# Version 1.2.5 - Nov 3, 2016
## Bug Fixes
    * Added crude support for source only Cocoapods to the IOSResolver.

# Version 1.2.4 - Oct 27, 2016
## Bug Fixes
    * Automated resolution of out of date pod repositories.

# Version 1.2.3 - Oct 25, 2016
## Bug Fixes
    * Fixed exception when reporting conflicting depedencies.

# Version 1.2.2 - Oct 17, 2016
## Bug Fixes
    * Fixed issue working with Unity 5.5
    * Fixed issue with PlayServicesResolver corrupting other iOS dependencies.
    * Updated build script to use Unity distributed tools for building.
# Version 1.2.1 - Jul 25, 2016
## Bug Fixes
   * Removed 1.2 Resolver and hardcoded whitelist of AARs to expand.
   * Improved error reporting when the "jar" executable can't be found.
   * Removed the need to set JAVA_HOME if "jar" is in the user's path.
   * Fixed spurious copying of partially matching AARs.
   * Changed resolver to only copy / expand when source AARs change.
   * Auto-resolution of dependencies is now performed when the Android
     build target is selected.
## New Features
   * Expand AARs that contain manifests with variable expansion like
     ${applicationId}.
   * Added optional logging in the JarResolverLib module.
   * Integration with the Android SDK manager for dependencies that
     declare required Android SDK packages.
# Version 1.2.0 - May 11 2016
## Bug Fixes
   * Handles resolving dependencies when the artifacts are split across 2 repos.
   * #4 Misdetecting version for versions like 1.2-alpha.  These are now string
       compared if alphanumeric
   * Removed resolver creation via reflection since it did not work all the time.
       Now a resolver needs to be loaded externally (which is existing behavior).
## New Features
    * Expose PlayServicesResolver properties to allow for script access.
    * Explodes firebase-common and firebase-measurement aar files to support
         ${applicationId} substitution.
# Version 1.1.1 - 25 Feb 2016
## Bug Fixes
    * #1 Spaces in project path not handled when exploding Aar file.
    * #2 Script compilation error: TypeLoadException.
# Version 1.1.0 - 5 Feb 2016
## New Features
  * Adds friendly alert when JAVA_HOME is not set on Windows platforms.
  * Adds flag for disabling background resolution.
  * Expands play-services-measurement and replaces ${applicationId} with the
            bundle Id.

 ## Bug Fixes
   * Fixes infinite loop of resolution triggered by resolution.
