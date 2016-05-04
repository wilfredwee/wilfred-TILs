# Restoring lost Windows boot files

Works for UEFI, GPT.

What this does is it adds Windows boot records to an EFI System Partition (that Windows automatically detects), even if the ESP is on a different drive than the drive than Windows in currently installed on.

1. Create Windows Live USB.
1. Use Live USB, go into Command Prompt.
1. Use diskpart to determine where your current Windows installation is.
1. Run: `bdcboot c:\windows /s c:` assuming your current Windows installation is at C:
1. Run : `bootrec /rebuildbcd`
1. This should add the Windows boot records to your ESP and you should be good to go.