#Installer and launcher documentation.

# What's included? #

  * `meld.exe` which checks if Python has been installed with Meld (if not, tries to use `PYTHON_HOME`), then launches Meld with pythonw.exe.  This can be located with the registry key `HKLM\Software\Meld\Executable`.
  * `meldc.exe` which checks if Python has been installed with Meld (if not, tries to use `PYTHON_HOME`), then launches Meld with python.exe.  This can be located with the registry key `HKLM\Software\Meld\CommandLineExecutable`.


# What's not included? #

  * Doesn't include [GNU Patch](http://savannah.gnu.org/projects/patch/) (to enable VCS browsing).
  * Portable zip is not completely portable (won't prevent the creation of `%APPDATA%\Meld\meldrc.ini`), it's simply a zip of what's in the installer.
  * Installer doesn't currently include multilingual support.

# Notes #
  * If upgrading from 1.6.1 (the first release of installer), you must first uninstall that version before installing a newer version.
  * If you choose not to install Python with Meld, you must make sure that your Python installation is setup properly (the launcher will not verify this).  Your installation should
    * Be Python 2
    * Include PyGTK (you'll probably want GTKSourceView as well)
    * Have `PYTHON_HOME` environment variable pointing to it