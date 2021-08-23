# Add Hackintosh Boot Option to ASRock UEFI
**Guide for motherboards like: ASRock 970 Extreme 4, ASRock 970 Pro 3 and other...**

Write to terminal:
`xcode-select --install
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Then, install Xcode from AppStore (for last macOS version) or download Xcode from https://developer.apple.com/download/more/ and place Xcode.app to the Applications folder.

After install Xcode, write to terminal:
`sudo xcode-select -s /Applications/Xcode.app/Contents/Developer
sudo xcodebuild -license accept`

* for macOS High Sierra and below
`brew tap vulgo/repo
brew install bootoption`

* for macOS Mojave, Catalina and above
`brew tap bootoption/repo
brew install bootoption`
 [Mount EFI partition](https://github.com/headkaze/EFI-Agent), and write to terminal:

* for Clover:
`sudo bootoption create -l /Volumes/EFI/EFI/CLOVER/CLOVERX64.EFI -d "macOS EFI"`

* for OpenCore: 
`sudo bootoption create -l /Volumes/EFI/EFI/OC/OpenCore.efi -d "macOS EFI"`

Reboot and open UEFI bios. Select “macOS EFI” in the boot priority menu.

Done.

##Credits:
[bootoption](https://github.com/bootoption)
[Homebrew](https://github.com/homebrew)
[EFI Agent](https://github.com/headkaze/EFI-Agent)
[ASRock](https://asrock.com)
[Apple](https://apple.com)
