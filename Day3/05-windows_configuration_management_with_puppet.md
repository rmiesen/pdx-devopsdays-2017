# Windows Configuration Management with Puppet
**Author:** Gene Liverman

## Better Together
 * (DSC, Hyper-V, SCCM, WMI) + Puppet
 * Can pull in powershell direclty to Puppet / Chef, and even do things more efficiently with Puppet / Chef.
 * Puppet + DSC.
   - DSA doesn't do everything Puppet does:
     + No reporting.
     + No Rebooting.
     + No pkg management
     + No historical data.
   - DSA, however, can do certain things better, like Hyper-V.
 * There will be cases where neither Puppet / Chef nor DSC provide a total solution. In this case, use them both together!

## Chocolatey
 * Basically `apt-get` / `dnf` for Windows
   - Builds on NuGet
   - provider for PackageManagement (OneGet) in WMF 5.
   - Public repo: chocolatey.org
   - Private repo: internal chocolatey server
     + great for internal software packages.
     + Module: chocolatey/chocolatey-server
 * Can get all sorts of open / closed source stuff there to (so long as it's "free as in beer")

## Patching
 * WSUS + strict change windows + Puppet
 * can be done either with embedded PowerShell scripts or via Puppet modules
   - Note taker's commentary: Chef can do all of this too with either embedded PowerShell or supermarket cookbooks.

## Puppet Development Kit
 * Everything you need to extend Puppet.
 * Takes care of environment setup.
 
