# discord.nvim-assets

assets for https://github.com/EpicBirb/discord.nvim for those who want to use icons from https://github.com/vscode-icons/vscode-icons because discord won't add support for svg and lottie has been tried on my end, doesn't work :(

You can make a contribution by submitting a pull request.
    - I would probably expect image file names to be corrected.

## Build Locally

##### prerequisites
1. go ahead and install the depedancies described in `pyproject.toml` (it's litterally just [python pillow](https://github.com/python-pillow/Pillow))
2. have `inkscape` (cli) in the project directory, it should look like this (if you are on windows):
    - `inkscape/bin/inkscape.com`

    if your cli executable is not `inkscape.com`, use the `--inkscape <path>` flag on `convert.py` to manually provide the path to the inkscape cli
3. also make sure you have git installed

##### now

then run the `fetch-icons.sh` script before running `convert.py` (you can use the `--help` flag on convert.py for additional options)

by default, only filename that start with `file_type_` will be converted, to include others, modify the entry for `include` in `patch.json` (the script will generate one if it's not present). add a entry to the list with the file name you want to also convert (filenames are shown in `vscode-icons/icons/` folder) (include the extension as well).

to rename the file after conversion, you can do so with the `rename` field in `patch.json`. where key is the original file name and the value is the renamed file name.

<h6>script poorly created by EpicBirb (go figure lol)</h6>
