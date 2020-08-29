# resolve-otio
An OpenTimelineIO plugin for DaVinci Resolve Studio. This is a just a simple project used to get familiar with the Python API in Resolve.

Currently only exporting is supported as the Resolve API doesn't have a way of laying out clips on the timeline.

## Installation

- `pip install opentimelineio`

- Copy the `otio.py` to the following location:

    **Mac OS X:** `/Library/Application Support/Blackmagic Design/DaVinci Resolve/Fusion/Scripts/Comp/` or `~/Library/Application Support/Blackmagic Design/DaVinci Resolve/Fusion/Scripts/Comp/`

    **Linux:** `/opt/resolve/Fusion/Scripts/Comp/` or `/home/resolve/Fusion/Scripts/Comp/` depending on installation

    **Windows:**    `%APPDATA%\Blackmagic Design\DaVinci Resolve\Fusion\Scripts\Comp\`

- Modify the sys.path.append line of the `otio.py` plugin to point to the location of the python site-packages where the OpenTimelineIO package is installed.

## Usage
### DaVinci Resolve
In DaVinci Resolve, open a Python console from *Workspace > Scripts > Console* and run the script with `exec(open("/PATH/TO/otio.py", "rb").read())`. This will open a window with two buttons. The first allows for selecting the export destination and the second performs the export.
### DaVinci Resolve Studio
From the DaVinci Resolve Studio menu select *Workspace > Scripts > otio*. This will open a window with two buttons. The first allows for selecting the export destination and the second performs the export.


## Limitations
- Only export is supported as the Resolve API currently isn't robust enough to import an OTIO
- This should work on *Windows* but no work or testing has taken place on *Windows*
